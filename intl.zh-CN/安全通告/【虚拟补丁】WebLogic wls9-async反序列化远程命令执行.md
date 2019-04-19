# 【虚拟补丁】WebLogic wls9-async反序列化远程命令执行 {#concept_186202 .concept}

2019年4月17日，阿里云云盾应急响应中心监测到国家信息安全漏洞共享平台（CNVD） 披露的“Oracle WebLogic wls9-async反序列化远程命令执行漏洞”。攻击者利用该漏洞可在未授权的情况下远程执行命令。

WebLogic部分版本中默认包含的wls9\_async\_response包，为WebLogic Server提供异步通讯服务。由于该War包在反序列化处理输入信息时存在缺陷，攻击者可以发送精心构造的恶意 HTTP 请求，获得目标服务器的权限，在未授权的情况下远程执行命令。

漏洞影响范围：Oracle WebLogic 10.X和Oracle WebLogic 12.1.3

危险等级：高危

规则防护：云防火墙虚拟补丁已支持防护

