# 【虚拟补丁】Confluence远程文件读取漏洞（CVE-2019-3396）

Confluence是一个专业的企业知识管理与协同软件，可用于构建企业wiki。

2019年4月4日，阿里云安全应急响应中心监测到Confluence官方发布安全更新，Widget Connector存在服务端模板注入漏洞，攻击者能利用此漏洞实现目录穿越遍历甚至远程命令执行。

近期阿里云安全应急响应中心监测到最新的漏洞利用方式流出，且多款蠕虫开始利用此漏洞进行传播。

漏洞详情请参见：[【漏洞预警】Confluence 远程命令执行高危漏洞（CVE-2019-3396）](https://help.aliyun.com/noticelist/articleid/1000128459.html)

漏洞危险等级：高危

规则防护：云防火墙虚拟补丁已支持防护

规则类型：命令执行

安全版本：

-   Version 6.6.12 and higher versions of 6.6.x
-   Version 6.12.3 and higher versions of 6.12.x
-   Version 6.13.3 and higher versions of 6.13.x
-   Version 6.14.2 and higher

