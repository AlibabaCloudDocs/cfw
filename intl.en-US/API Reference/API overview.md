# API overview

The following tables list API operations available for use in Cloud Firewall.

## Firewall enabling and disabling

|Operation|Description|
|---------|-----------|
|[PutEnableFwSwitch](/intl.en-US/API Reference/Firewall switch/PutEnableFwSwitch.md)|Enables a firewall for the specified asset.|
|[PutDisableFwSwitch](/intl.en-US/API Reference/Firewall switch/PutDisableFwSwitch.md)|Disables a firewall for the specified asset.|
|[PutEnableAllFwSwitch](/intl.en-US/API Reference/Firewall switch/PutEnableAllFwSwitch.md)|Enables a firewall for all assets.|
|[PutDisableAllFwSwitch](/intl.en-US/API Reference/Firewall switch/PutDisableAllFwSwitch.md)|Disables a firewall for all assets.|

## Access control

|Operation|Description|
|---------|-----------|
|[AddControlPolicy](/intl.en-US/API Reference/Access control/AddControlPolicy.md)|Creates an access control policy.|
|[DescribeControlPolicy](/intl.en-US/API Reference/Access control/DescribeControlPolicy.md)|Queries the information about all access control policies.|
|[DescribeDomainResolve](/intl.en-US/API Reference/Access control/DescribeDomainResolve.md)|Queries the DNS resolution result of a domain name.|
|[DescribePolicyPriorUsed](/intl.en-US/API Reference/Access control/DescribePolicyPriorUsed.md)|Queries the priority range of access control policies.|
|[ModifyControlPolicy](/intl.en-US/API Reference/Access control/ModifyControlPolicy.md)|Modifies the configurations of an access control policy.|
|[ModifyControlPolicyPosition](/intl.en-US/API Reference/Access control/ModifyControlPolicyPosition.md)|Modifies the priority of an access control policy.|
|[DeleteControlPolicy](/intl.en-US/API Reference/Access control/DeleteControlPolicy.md)|Deletes an access control policy.|
|[DescribePolicyAdvancedConfig](/intl.en-US/API Reference/Access control/Strict mode/DescribePolicyAdvancedConfig.md)|Queries the status of the strict mode for an access control policy.|
|[ModifyPolicyAdvancedConfig](/intl.en-US/API Reference/Access control/Strict mode/ModifyPolicyAdvancedConfig.md)|Enables or disables the strict mode for an access control policy.|

## VPC firewalls

|Operation|Description|
|---------|-----------|
|[CreateVpcFirewallControlPolicy](/intl.en-US/API Reference/Access control/VPC firewalls/CreateVpcFirewallControlPolicy.md)|Creates an access control policy for the specified VPC firewall policy group.|
|[DescribeVpcFirewallControlPolicy](/intl.en-US/API Reference/Access control/VPC firewalls/DescribeVpcFirewallControlPolicy.md)|Queries the information about all access control policies of the specified VPC firewall.|
|[DescribeVpcFirewallPolicyPriorUsed](/intl.en-US/API Reference/Access control/VPC firewalls/DescribeVpcFirewallPolicyPriorUsed.md)|Queries the priority range of access control policies in the specified VPC firewall policy group.|
|[DescribeVpcFirewallAclGroupList](/intl.en-US/API Reference/Access control/VPC firewalls/DescribeVpcFirewallAclGroupList.md)|Queries the information about all access control policy groups of the VPC firewall.|
|[ModifyVpcFirewallControlPolicy](/intl.en-US/API Reference/Access control/VPC firewalls/ModifyVpcFirewallControlPolicy.md)|Modifies the configurations of an access control policy in the specified VPC firewall policy group.|
|[ModifyVpcFirewallControlPolicyPosition](/intl.en-US/API Reference/Access control/VPC firewalls/ModifyVpcFirewallControlPolicyPosition.md)|Modifies the priority of an access control policy in the specified VPC firewall policy group.|
|[ResetVpcFirewallRuleHitCount](/intl.en-US/API Reference/Access control/VPC firewalls/ResetVpcFirewallRuleHitCount.md)|Clears the hits of an access control policy in the specified VPC firewall policy group.|
|[DeleteVpcFirewallControlPolicy](/intl.en-US/API Reference/Access control/VPC firewalls/DeleteVpcFirewallControlPolicy.md)|Deletes an access control policy in the specified VPC firewall policy group.|

## Address books

|Operation|Description|
|---------|-----------|
|[AddAddressBook](/intl.en-US/API Reference/Address books/AddAddressBook.md)|Creates an access control address book, such as an IP address book, ECS tag address book, port address book, and domain address book.|
|[DescribeAddressBook](/intl.en-US/API Reference/Address books/DescribeAddressBook.md)|Queries details of an access control address book.|
|[ModifyAddressBook](/intl.en-US/API Reference/Address books/ModifyAddressBook.md)|Modifies an access control address book.|
|[DeleteAddressBook](/intl.en-US/API Reference/Address books/DeleteAddressBook.md)|Deletes an access control address book.|

