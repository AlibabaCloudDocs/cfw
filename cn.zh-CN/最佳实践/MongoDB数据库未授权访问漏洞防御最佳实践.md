# MongoDB数据库未授权访问漏洞防御最佳实践 {#concept_cpt_f2t_2hb .task}

MongoDB数据库未授权访问漏洞可以导致数据库数据泄露或被删除勒索。

为保证您的业务和应用的安全，云防火墙提供以下漏洞修复指导方案。

MongoDB服务安装完成后，会默认存在一个admin数据库，该admin数据库内容未空，并且没有记录任何权限相关的信息。

MongoDB默认设置为无权限访问限制，也就是说开启MongoDB服务时如果不添加任何参数，默认是不需要权限验证的。因此，登录的用户无需密码，即可通过默认端口对数据库任意操作（增、删、改、查等高危操作），并可远程访问数据库。

因此，加固的核心操作是实现在admin.system.users中添加用户，这样MongoDB的认证、授权服务才能生效。

## 修复方案 {#section_ht2_kbk_49b .section}

1.  **配置云防火墙访问控制策略。** 
    1.  **限定MongoDB服务仅对内网服务器提供服务** 

        在云防火墙控制台 **网络流量分析** \> **互联网访问活动** \> **开放应用**页面，查看公网中MongoDB服务所属的IP地址。如果该服务仅对内网服务器提供服务，建议禁止将MongoDB服务开放到互联网上。

        ![定位MongoDB](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/149039/156704344341436_zh-CN.png)

        执行以下命令启动IP地址绑定、限定该MongoDB服务仅对内网服务器提供服务（本示例中MongoDB数据库实例将只监听1.2.3.4内网的请求）。

        ``` {#codeblock_7tm_59k_nq9}
        mongod --bind_ip 1.2.3.4
        ```

    2.  **配置MongoDB云防火墙访问控制策略只对可信源放行。** 

        在云防火墙控制台 **安全策略** \> **访问控制** \> **互联网边界防火墙** \> **外对内**页面，配置访问控制策略，仅允许与MongoDB数据库依赖的服务器访问该MongoDB服务。

        1.  将MongoDB所有可信源加入地址簿。

            ![将MongoDB所有可信源加入地址簿](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/149039/156704344341444_zh-CN.png)

        2.  对MongoDB可信源进行放行。

            ![对MongoDB可信源进行放行](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/149039/156704344441446_zh-CN.png)

            -   **访问源**：选择已配置好的MongoDB所有可信源地址簿。
            -   **目的**：为MongoDB可信源地址。
            -   **协议类型**：选择TCP协议，表示互联网访问流量。
            -   **端口**： 设置为0/0，表示可信源的所有端口地址。
    3.  **拒绝所有其他非可信源访问MongoDB服务。** 

        ![拒绝所有其他非可信源访问MongoDB服务](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/149039/156704344441455_zh-CN.png)

        -   **访问源**：设置为Any，表示所有访问源。
        -   **目的**：为MongoDB 服务所属的公网IP地址。
        -   **协议类型**：选择TCP协议，表示互联网访问流量。
        -   **端口**： 设置为0/0，表示非可信源的所有端口地址。
2.  **开启基于权限角色的登录认证功能。** 

    1.  执行以下命令，在未开启认证的环境下登录到数据库。

        ``` {#codeblock_hxf_lk0_17i}
        [mongodbrac3 bin]$ ./mongo 127.0.0.1:27028 (此处修改了默认端口)
        MongoDB shell version: 2.0.1
        connecting to: 127.0.0.1:27028/test
        ```

    2.  执行以下命令切换到admin数据库。

        ``` {#codeblock_gyb_xk9_9el}
        > use admin
        switched to db admin
        ```

        **说明：** 只有切换到admin数据库后添加的账号才是管理员账号。

    3.  执行以下命令创建为admin数据库创建管理员用户。 本示例中用户名为supper，密码supWDxsf67%H。

        **说明：** MongoDB从V3版本开始取消使用addUser方法、采用db.createUser命令创建用户。

        ``` {#codeblock_p0w_29k_2lz}
        > db.addUser("supper", "supWDxsf67%H") 或
        { "n" : 0, "connectionId" : 4, "err" : null, "ok" : 1 }
        > db.createUser({user:"****",pwd:"***********",roles:["root"]})
        {
        "user" : "****",
        "readOnly" : false,
        "pwd" : "**************","_id"
        ObjectId("4f2bc0d357a309043c6947a4")
        }
        #管理员账号在system.users中。
        > db.getCollectionNames()
        [ "system.indexes", "system.users", "system.version" ]
        ```

        创建的用户账号存在system.users中。

        **说明：** 管理员账号不要设置为常见账号；密码需要满足一定的复杂度：长度至少八位以上并包括大小写字母、数字、特殊字符混合体，不要使用生日、姓名、身份证编号等常见密码。

    4.  验证之前添加的用户是否创建成功。

        执行命令后，返回1，表示用户已创建成功。

        ``` {#codeblock_xvt_c3s_ywu}
        > db.auth("supper","supWDxsf67%H")
        1
        								
        ```

    5.  结束Mongodb进程并重启Mongodb服务。

        ``` {#codeblock_aa0_mqr_lvy}
        > db.auth("supper","supWDxsf67%H")
        > exit
        bye
        ```

    6.  执行以下命令，启动用户权限认证。

        开启用户权限认证后，未登录的客户端就没有权限做任何操作。

        ``` {#codeblock_klg_lbp_gh7}
        > mongod --dbpath=/path/mongodb --bind_ip=10.0.0.1 --port=27028 --fork=true logpath=/path/mongod.log --auth&
        ```

    **说明：** 

    -   admin.system.users中将会保存比在其它数据库中设置的用户权限更大的用户信息，拥有超级权限，也就是说在admin中创建的用户可以对MongoDB中的其他数据库数据进行操作。
    -   MongoDB系统中，数据库是由超级用户来创建的，一个数据库可以包含多个用户，一个用户只能在一个数据库下，不同数据库中的用户可以同名。
    -   特定数据库（例如：DB1）的用户User1不能够访问其他数据库DB2，但是可以访问本数据库下其他用户创建的数据。
    -   不同数据库中同名的用户不能够登录其他数据库，例如：DB1、DB2都有user1，以user1登录DB1后，不能登录到DB2进行数据库操作。
    -   在admin数据库创建的用户具有超级权限，可以对MongoDB系统内的任何数据库的数据对象进行操作。
    -   使用db.auth\(\)可以对数据库中的用户进行验证，如果验证成功则返回1，否则返回0。db.auth\(\)只能针对登录用户所属的数据库的用户信息进行验证，不能验证其他数据库的用户信息。

## 检测是否存在入侵风险 {#section_87n_2i2_b59 .section}

如果您是MongoDB数据库管理员，可使用以下方式确认是否有进一步的入侵行为：

-   查看MongoDB的日志是否完整，并确认执行删除数据库的源IP地址和时间、行为。
-   使用db.system.users.find\(\)命令检查MongoDB帐户是否存在未添加密码的账户。
-   使用db.fs.files.find\(\)命令检查GridFS是否有人存储了任何文件。
-   使用show log global命令查看日志文件，确认是否有其他用户访问了MongoDB。

