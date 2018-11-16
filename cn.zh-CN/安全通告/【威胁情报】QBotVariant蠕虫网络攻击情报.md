# 【威胁情报】QBotVariant蠕虫网络攻击情报 {#concept_kz2_zjz_5fb .concept}

阿里云安全在今年5月份监测到了一种改写自互联网公开渠道源码的蠕虫样本，我们将该类样本命名为QBotVariant。QBotVariant具有DDoS攻击、后门、下载器和破解等功能，一旦被入侵便变会肉鸡。QBotVariant可在互联网上广泛传播并造成极大的危害。

QBotVariant传播的方式有两种：一是利用Hadoop Yarn资源管理系统REST API未授权访问漏洞进行入侵；二是通过硬编码的弱密码进行SSH暴力破解。一旦感染此类蠕虫，不仅会占用主机计算资源消耗带宽流量，成为攻击其他主机的肉鸡，还可能造成数据泄露、数据丢失等后果。

事件：蠕虫攻击

威胁等级：高危

云防火墙已可防御此类攻击，建议用户开启云防火墙的[入侵防御能力](../../../../cn.zh-CN/用户指南/安全策略/入侵防御策略.md#ol_ez3_mzd_dfb)。

详见[部分恶意URL及QBotVariant详情](https://yq.aliyun.com/articles/667970)。

