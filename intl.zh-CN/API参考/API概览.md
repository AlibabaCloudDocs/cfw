# API概览

本文列举了云防火墙提供的所有API接口，方便您查询使用。

## 防火墙开关API

|API|描述|
|---|--|
|[PutEnableFwSwitch]()|为指定资产开启防火墙开关。|
|[PutDisableFwSwitch]()|为指定资产关闭防火墙开关。|
|[PutEnableAllFwSwitch]()|为所有资产开启防火墙开关。|
|[PutDisableAllFwSwitch]()|为所有资产关闭防火墙开关。|

## 访问控制API

|API|描述|
|---|--|
|[AddControlPolicy](/intl.zh-CN/API参考/访问控制/AddControlPolicy.md)|添加访问控制策略。|
|[DescribeControlPolicy](/intl.zh-CN/API参考/访问控制/DescribeControlPolicy.md)|获取所有访问控制策略信息。|
|[DescribeDomainResolve](/intl.zh-CN/API参考/访问控制/DescribeDomainResolve.md)|获取域名DNS的解析结果。|
|[DescribePolicyPriorUsed](/intl.zh-CN/API参考/访问控制/DescribePolicyPriorUsed.md)|查询访问控制策略优先级生效范围。|
|[ModifyControlPolicy](/intl.zh-CN/API参考/访问控制/ModifyControlPolicy.md)|修改安全访问控制策略的配置信息。|
|[ModifyControlPolicyPosition](/intl.zh-CN/API参考/访问控制/ModifyControlPolicyPosition.md)|修改访问控制策略的优先级。|
|[DeleteControlPolicy](/intl.zh-CN/API参考/访问控制/DeleteControlPolicy.md)|删除访问控制策略。|
|[DescribePolicyAdvancedConfig](/intl.zh-CN/API参考/访问控制/严格模式/DescribePolicyAdvancedConfig.md)|查询访问控制策略严格模式的开启状态。|
|[ModifyPolicyAdvancedConfig](/intl.zh-CN/API参考/访问控制/严格模式/ModifyPolicyAdvancedConfig.md)|开启或关闭访问控制策略严格模式。|

## VPC边界防火墙API

|API|描述|
|---|--|
|[CreateVpcFirewallControlPolicy](/intl.zh-CN/API参考/访问控制/VPC边界防火墙/CreateVpcFirewallControlPolicy.md)|为指定VPC防火墙策略组添加访问控制策略。|
|[DescribeVpcFirewallControlPolicy](/intl.zh-CN/API参考/访问控制/VPC边界防火墙/DescribeVpcFirewallControlPolicy.md)|查询指定的VPC边界防火墙所有的访问控制策略信息。|
|[DescribeVpcFirewallPolicyPriorUsed](/intl.zh-CN/API参考/访问控制/VPC边界防火墙/DescribeVpcFirewallPolicyPriorUsed.md)|查询指定VPC防火墙策略组访问控制策略优先级生效范围。|
|[DescribeVpcFirewallAclGroupList](/intl.zh-CN/API参考/访问控制/VPC边界防火墙/DescribeVpcFirewallAclGroupList.md)|获取VPC防火墙所有访问控制策略组信息。|
|[ModifyVpcFirewallControlPolicy](/intl.zh-CN/API参考/访问控制/VPC边界防火墙/ModifyVpcFirewallControlPolicy.md)|修改指定VPC防火墙策略组的访问控制策略的配置信息。|
|[ModifyVpcFirewallControlPolicyPosition](/intl.zh-CN/API参考/访问控制/VPC边界防火墙/ModifyVpcFirewallControlPolicyPosition.md)|修改指定VPC防火墙策略组访问控制策略的优先级。|
|[ResetVpcFirewallRuleHitCount](/intl.zh-CN/API参考/访问控制/VPC边界防火墙/ResetVpcFirewallRuleHitCount.md)|将指定的VPC防火墙策略组访问控制策略的命中计数清零。|
|[DeleteVpcFirewallControlPolicy](/intl.zh-CN/API参考/访问控制/VPC边界防火墙/DeleteVpcFirewallControlPolicy.md)|删除指定VPC防火墙策略组的访问控制策略。|

## 地址簿API

|API|描述|
|---|--|
|[AddAddressBook](/intl.zh-CN/API参考/地址簿/AddAddressBook.md)|添加安全访问控制地址簿，包括IP地址簿、ECS标签地址簿、端口地址簿和域名地址簿。|
|[DescribeAddressBook](/intl.zh-CN/API参考/地址簿/DescribeAddressBook.md)|查询安全访问控制地址簿的详细信息。|
|[ModifyAddressBook](/intl.zh-CN/API参考/地址簿/ModifyAddressBook.md)|修改安全访问控制的地址簿。|
|[DeleteAddressBook](/intl.zh-CN/API参考/地址簿/DeleteAddressBook.md)|删除安全访问控制的地址簿。|

