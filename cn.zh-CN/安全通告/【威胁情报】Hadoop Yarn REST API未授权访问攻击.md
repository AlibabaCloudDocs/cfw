# 【威胁情报】Hadoop Yarn REST API未授权访问攻击 {#concept_kns_ftw_4fb .concept}

阿里云云防火墙可防护Hadoop Yarn REST API未授权访问攻击。

Hadoop是一款由Apache基金会推出的分布式系统框架，通过MapReduce 算法进行分布式处理。Yarn是Hadoop集群的资源管理系统存在漏洞的主机，攻击者无需认证即可通过REST API部署任务来执行任意指令，最终完全控制服务器。

2018年10月25日监控到大量利用Hadoop Yarn REST API未授权访问漏洞的攻击事件。攻击成功后，受控主机会访问恶意源：hxxps://bitbucket.org/\*/raw/master/zz.sh 下载恶意文件后进行挖矿。

云防火墙已可防御此类攻击。

事件：Hadoop Yarn REST API未授权访问攻击

威胁等级：高级

