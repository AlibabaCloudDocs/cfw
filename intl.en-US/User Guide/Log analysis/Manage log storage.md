# Manage log storage {#concept_s2n_dl4_hhb .concept}

After you enable the Log Analysis function of Cloud Firewall, the log storage space is allocated based on your specified log storage size. You can view the usage of the log storage space on the **Log Analysis** page in the Cloud Firewall console.

## Chethe log storage {#section_obl_hnz_qfb .section}

You can view the log storage in the Cloud Firewall console at any time.

**Note:** The log storage information in the console is not updated in real time. It takes up to two hours to update the actual storage information to the console. We recommend that you expand the log storage space before it is exhausted.

1.  Log on to the [Cloud Firewall console](https://partners-intl.console.aliyun.com/#/cfwnext).
2.  In the left-side navigation pane, select **Advanced Features** \> **Log Analysis**.
3.  View the log storage information in the upper-right corner of the Log Analysis page.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/154334/155922543143271_en-US.png)


## Expand log storage {#section_uqq_2rz_qfb .section}

To expand the log storage, click **Upgrade Storage** at the top of the Log Analysis page.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/154334/155922543248324_en-US.png)

**Note:** We recommend that you expand the log storage space before it is exhausted. If no storage space is available, then the new log data cannot be written into the dedicated Logstore.

## Clear log storage {#section_gsv_lsz_qfb .section}

You can delete all log entries stored in the Logstore. For example, you can delete the log entries generated during the testing phase and use the log storage space to store log entries that are generated during the production phase only.

Click **Clear** at the top of the Log Analysis page, and confirm to delete all stored log entries.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/154334/155922543248325_en-US.png)

**Notice:** You cannot recover the deleted log entries. This operation is irreversible.

**Note:** You only have limited times for clearing the log storage.

