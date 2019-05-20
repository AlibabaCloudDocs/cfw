# Overview {#concept_dfs_pxj_hhb .concept}

The Log Analysis service of Cloud Firewall provides internet traffic logs and real-time log analysis.

The Log Analysis service of Cloud Firewall can automatically collect and store real-time log of both inbound and outbound traffic. It outputs query analysis, reports, alarms, and downstream computing interconnection and provide you with detailed analysis result.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/154090/155834266747615_en-US.png)

## Benefits {#section_nx2_jxn_rx8 .section}

The Log Analysis service of Cloud Firewall has the following benefits:

-   **Classified Protection compliance**: Log Analysis provides log storage duration of six months to help your website meet the requirements of classified protection compliance.
-   **Easy configuration**: Easy configuration allows you to collect Internet traffic logs in real time.
-   **Real-time analysis**: Integrated with the Simple Log Service \(SLS\), the Log Analysis service provides the real-time log analysis service and report center. With the help of log analysis, you can view all the traffic and user's visits going through Cloud Firewall.
-   **Real-time alarms**: Log Analysis supports you to customize real-time monitoring and alerts based on specific indicators. This ensures you receive real-time alerts when there is any threats detected in the critical business.

## Prerequisites {#section_mxf_3pd_2gb .section}

Before you begin to use the service of Log Analysis, the following prerequisite must be available:

-   You have purchased and activated the Log Analysis service of Cloud Firewall \(Log Analysis is available in Pro, Enterprise, and Flagship editions\). For details, refer to [Enable the log analysis service](reseller.en-US/.md#).

## Restrictions {#section_g7p_mg6_fop .section}

The logstore of Cloud Firewall is an exclusive logstore with the following restrictions:

-   You cannot write data into logstore with APIs or SDKs, or modify the attributes of the logstore \(such as the storage cycle\).

    **Note:** Other general logstore features \(such as query, statistics, alarms, and stream consumption\) are supported, and there is no difference with the general logstore.

-   Alibaba Cloud's Log Service \(SLS\) does not charge for the exclusive logstore of Cloud Firewall, but SLS itself must be available \(not overdue\).
-   Built-in reports provided by Log Analysis of Cloud Firewall may be updated and upgraded automatically.

## Scenarios {#section_yyw_kpd_2gb .section}

-   Track Internet traffic logs to trace security threats.
-   Allow you to view Internet request activities in real time, and check the security status and trend of your assets.
-   Provide you with quick understanding of security operation efficiency and handling the risks in a timely manner.
-   Output logs to your self-built data and computing centers.

