# Export log entries {#concept_zp1_s24_hhb .concept}

The Log Analysis function of Cloud Firewall allows you to export log entries to your local device.

You can export log entries on the current page to a CSV file, or export all log entries to a TXT file.

## Procedure {#section_clk_gvk_kfb .section}

1.  Log on to the [Cloud Firewall console](https://partners-intl.console.aliyun.com/#/cfwnext).
2.  In the left-side navigation pane, select **Advanced Features** \> **Log Analysis**.
3.  On the Raw Logs tab page, click the **Download** icon ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/154313/156825345743249_en-US.png)on the right side.

    **Note:** The download icon does not appear if there's no search result.

4.  In the Log Download dialog box, select **Download Log in Current Page** or **Download all logs by the CLI console**.
    -   **Download logs in current page**:

        Click **OK** to export the raw log entries on the current page to a CSV file.

    -   **Download all logs by CLI**:

        1.  For more information about installing the CLI, see [CLI guide](https://github.com/aliyun/aliyun-log-cli/blob/master/README.md#installation).
        2.  Click [Security Information Management Link](https://usercenter.console.aliyun.com/#/manage/ak) to view and record the AccessKey ID and AccessKey Secret of the current user.
        3.  Click **Copy Command** and paste the command into CLI, replace the `AccessID obtained in step 2`and `AccessKey Secret obtained in step 2` with the AccessKey ID and AccessKey Secret of the current user, and run the command.
        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/154313/156825345743250_en-US.png)

        After you run the command, all raw log entries created by Cloud Firewall are automatically exported and saved to the file download\_data.txt.


