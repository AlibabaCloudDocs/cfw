# 【威胁情报】Hadoop Yarn REST API未授权访问攻击

阿里云云防火墙可防护Hadoop Yarn REST API未授权访问攻击。

Hadoop是一款由Apache基金会推出的分布式系统框架，通过MapReduce算法进行分布式处理。Yarn是Hadoop集群的资源管理系统存在漏洞的主机，攻击者无需认证即可通过REST API部署任务来执行任意指令，最终完全控制服务器。

2018年10月25日阿里云监控到大量利用Hadoop Yarn REST API未授权访问漏洞的攻击事件。攻击成功后，受控主机会访问恶意源hxxps://bitbucket.org/\*/raw/master/zz.sh下载恶意文件后进行挖矿。

漏洞危险等级：高危

规则防护：云防火墙虚拟补丁已支持防护

事件：Hadoop Yarn REST API未授权访问攻击

