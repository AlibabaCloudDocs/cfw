# Authorize Cloud Firewall {#concept_nfn_xks_ngb .concept}

In the latest version of Cloud Firewall, the **Internet access analysis** feature is included. To enable this feature, Cloud Firewall has to display your IP addresses and port information. Therefore, you must grant Cloud Firewall the permission to call the SLB API.

## Background {#section_pvs_k3z_ngb .section}

To grant Cloud Firewall the access to cloud resources, you must have one of the following accounts:

-   An Alibaba Cloud primary account
-   A RAM user account with the AliyunRAMFullAccess permission

**Note:** You cannot use a [RAM user account](../../../../intl.en-US/User Guide/Permission management/Permission granting/Permission granting in RAM.md#) without the AliyunRAMFullAccess permission to grant Cloud Firewall the access to cloud resources.

## Authorization procedure {#section_ktp_4ns_ngb .section}

1.  Click **Confirm Authorization Policy**.

    This grants Cloud Firewall the following permissions:

    -   **AliyunCloudFirewallAccessingECSRole**: Allows Cloud Firewall to access ECS instances.
    -   **AliyunCloudFirewallDefautlRole**: Allows Cloud Firewall to access other cloud services, such as OSS and SLB.
    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/116911/155652456637959_en-US.png)

    After the authorization is complete, the system automatically returns to the Cloud Firewall console.

    **Note:** **AliyunCloudFirewallAccessingECSRole** and **AliyunCloudFirewallDefautlRole** are default permissions and are both required.


