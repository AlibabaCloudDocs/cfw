# 【基础规则】Microsoft SQL Server xp\_cmdshell远程命令执行

xp\_cmdshell可能被攻击者恶意利用SQL Server运行权限执行系统命令。SQL Server是Microsoft公司推出的关系型数据库管理系统，xp\_cmdshell是SQL Server运行系统命令行的系统存储过程。xp\_cmdshell可以让系统管理员以操作系统命令行解释器的方式执行给定的命令字符串，并以文本行方式返回任何输出。

漏洞影响范围：Microsoft SQL Server。

漏洞危险等级：高危

规则防护：防护由SQL Server xp\_cmdshell导致的远程命令执行。

规则类型：命令执行

