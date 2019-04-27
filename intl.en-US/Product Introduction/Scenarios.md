# Scenarios {#concept_imn_nlj_bfb .concept}

Cloud Firewall is the primary infrastructure that you need to deploy to ensure network security of the businesses when you have migrated onto Alibaba Cloud. Cloud Firewall supports the functions including network-wide traffic identification, centralized policy management, intrusion detection, and logging.

Cloud Firewall controls the access traffic from the Internet to your ECS instances, external connection traffic from ECS instances to the Internet, and access traffic between ECS instances.

Cloud Firewall applies to the following scenarios:

-   **Control the access traffic from the Internet to ECS instances**: For example, a financial company on Alibaba Cloud uses IPS to protect their HTTP and other businesses exposed on the Internet.
-   **Prevent abnormal external connection activities**: For example, a government sector on Alibaba Cloud analyzes not only the access traffic from the Internet to ECS instances, but also the external connection traffic from ECS instances to the Internet. Based on the analysis, the government sector can determine which ECS instances are at risk and then block abnormal access in real time to avoid potential risks.
-   **Protect the access traffic between ECS instances through micro-isolation**: For example, an e-commerce company on Alibaba Cloud runs businesses based on HTTP and uses Web Application Firewall \(WAF\) for business protection. To isolate the different businesses from each other, the company now deploys Cloud Firewall to comprehensively improve network control. This helps avoid threats to the company's cloud-based businesses due to security risks on a certain ECS instance.

