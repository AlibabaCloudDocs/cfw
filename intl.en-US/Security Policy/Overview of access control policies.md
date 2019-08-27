# Overview of access control policies {#concept_yjq_tdg_nfb .concept}

You can configure access control policies in Cloud Firewall to restrict the inbound and outbound traffic of your servers. This helps reduce the risk of intrusions.

## Limits on the number of access control policies in each Cloud Firewall edition {#section_zpw_8dv_s35 .section}

The maximum number of access control policies varies with the Cloud Firewall edition.

-   In **Pro** Edition, you can configure up to 1,000 outbound policies and 1,000 inbound policies.
-   In **Enterprise** Edition, you can configure up to 2,000 outbound policies and 2,000 inbound policies.
-   In **Flagship** Edition, you can configure up to 5,000 outbound policies and 5,000 inbound policies.

**Note:** Cloud Firewall allows you to control the traffic bound to specified domains. After you configure an access control policy for a domain, all traffic bound to this domain is controlled. The policy actions include **Allow**, **Deny**, and **Monitor**.

## Limits on the number of internal firewall policies {#section_u6e_rp8_t27 .section}

By default, you can create up to 100 policy groups and 100 policies between your servers. The policies include those created in the ECS security group module and synchronized to Cloud Firewall and those created on the Internal Firewall page in Cloud Firewall.

**Note:** If you want to create more policies than allowed, we recommend that you delete unnecessary policies or submit a ticket for technical support.

