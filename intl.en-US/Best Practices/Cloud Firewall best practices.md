# Cloud Firewall best practices {#concept_kqt_pkr_cfb .concept}

## How to choose the appropriate Cloud Firewall edition {#section_w5s_w4r_cfb .section}

Cloud Firewall includes the Advanced Edition, Enterprise Edition, and Flagship Edition. The features and asset or bandwidth scaling specifications vary according to the edition. For more information, see [Features](../../../../reseller.en-US/Product Introduction/Features.md#table_qsv_slr_cfb).

## Configure access policies for out-in traffic {#section_ytv_xkr_cfb .section}

In access policies for out-in traffic, do not allow access to all ports from public IP addresses. Open only necessary Internet IP addresses and ports. **Block** access to all the other ports.

1.  Allow access traffic to necessary applications or ports.

    On the **Access Control** page, click the **Out-In Traffic** tab. Add an access policy. Set the source to `0.0.0.0/0` or a specific IP address. You can also set the source to the default address book **ANY** \(`0.0.0.0/0`\) or a specific IP address. Set the destination to the IP address that needs to be accessed or a specific IP address. Set the protocol to **ANY** or a specific protocol based on business requirements. Set the action to **Allow**.

    ![选择](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21289/156819507235632_en-US.png)

    Example:

    Port 80 is a Web service port that needs to be opened to all public IP addresses. Therefore, set the source to 0.0.0.0/0 for port 80. Ports 1433 and 3389 are SQL Server and RDP service ports, respectively. They are opened only to specific sources. Therefore, set the source to the specific sources for ports 1433 and 3389 respectively.

2.  Block all the other out-in traffic.

    On the **Access Control** page, click the **Out-In Traffic** tab. Add an access policy. Set the source to `0.0.0.0/0` or the default address book **ANY** \(`0.0.0.0/0`\). Set both the destination and protocol to **ANY**. Set the action to **Block**.


## Configure access policies for in-out traffic {#section_wcn_xkr_cfb .section}

We recommend that you do not allow all **in-out traffic**. Instead, allow only outbound access traffic to necessary public IP addresses or domain names, and **block** all the other in-out traffic.

1.  Allow outbound access traffic from necessary applications or ports.

    On the **Access Control** page, click the **In-Out Traffic** tab. Add an access policy. Set the source to `0.0.0.0/0` or a specific IP address. You can also set the source to the default address book **ANY** \(`0.0.0.0/0`\) or a specific IP address. Set the destination to the domain name or IP address that needs to be accessed or a specific IP address. Set the protocol to ANY or a specific protocol based on business requirements. Set the action to Allow.

2.  **Block** all the other in-out traffic.

    On the Access Control page, click the In-Out Traffic tab. Add an access policy. Set the source to `0.0.0.0/0` or the default address book **ANY** \(`0.0.0.0/0`\). Set both the destination and protocol to **ANY**. Set the action to **Block**.


## Enable Cloud Firewall protection and the interception mode for intrusion prevention {#section_ngk_1lr_cfb .section}

After subscribing to the Cloud Firewall service, you can click **Protect All** on the **Firewall Switch** page and click **Interception Mode** on the **Intrusion Prevention** page. In this way, you can fully protect the security of your assets.

