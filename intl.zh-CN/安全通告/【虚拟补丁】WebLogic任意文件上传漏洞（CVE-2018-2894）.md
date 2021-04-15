# 【虚拟补丁】WebLogic任意文件上传漏洞（CVE-2018-2894）

阿里云云防火墙支持防护WebLogic任意文件上传漏洞。

WebLogic是由美国Oracle公司推出的application server，是基于JAVAEE架构的中间件。WebLogic是用于开发、集成、部署和管理大型分布式Web应用、网络应用和数据库应用的Java应用服务器。

ws\_utc为WebLogic Web服务测试客户端，其配置页面存在未授权访问的问题，路径为 /ws\_utc/config.do。攻击者可通过访问此配置页面，用有效的WebLogic Web路径替换存储JKS Keystores的文件目录，然后上传恶意的JSP脚本木马文件。

影响范围：

-   WebLogic 10.3.6.0
-   WebLogic 12.1.3.0
-   WebLogic 12.2.1.2
-   WebLogic 12.2.1.3

漏洞危险等级：高危

规则防护：云防火墙虚拟补丁已支持防护

规则类型：命令执行

