# Relationship between Cloud Firewall and Alibaba Cloud products {#concept_atr_pnw_tgb .concept}

## Cloud Firewall is deployed on Alibaba Cloud. {#section_fgw_snw_tgb .section}

The following figure shows the logical relationships between Cloud Firewall and some of the Alibaba Cloud products.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/124493/155650673338794_en-US.png)

## Work with other security products such as Web Application Firewall \(WAF\) and Anti-DDoS Protection {#section_mdq_y1f_vgb .section}

The figure above shows that Cloud Firewall is used to protect the source IP addresses of WAF and Anti-DDoS Protection.

## Work with Content Delivery Network \(CDN\) {#section_lkt_z1f_vgb .section}

Cloud Firewall is used to protect source IP addresses.

## Work with Object Storage Service \(OSS\) and ApsaraDB RDS {#section_hby_z1f_vgb .section}

Cloud Firewall currently does not support protecting OSS and ApsaraDB RDS instances. This feature will be available in the second half of 2019.

## Work with Bastionhost {#section_nsy_z1f_vgb .section}

Cloud Firewall currently does not support protecting bastionhost.

## Work with VPC Gateway {#section_zhz_z1f_vgb .section}

Cloud Firewall currently does not support protecting VPC gateways.

## Work with Server Load Balancer \(SLB\) {#section_lvz_z1f_vgb .section}

SLB instances include internet SLB instances and intranet SLB instances. Cloud Firewall currently does not support protecting internet SLB instances. It only supports protecting intranet SLB instances with EIPs.

