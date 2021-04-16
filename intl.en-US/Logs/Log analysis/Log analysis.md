# Log analysis

Could Firewall console supports the Log Analysis function.

## Overview

After you enable the Log Analysis function in Cloud Firewall console, you can perform real-time log search and analysis, view or edit dashboards, and set up monitoring and alerts on the Log Analysis page.

## Procedure

1.  Log on to the [Cloud Firewall console](https://yundunnext.console.aliyun.com/?p=cfwnext).
2.  In the left-side navigation pane, select **Logs** \> **Log Analysis**.
3.  Click the **Status** switch on the right side to enable the Log Analysis function.

    ![状态](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/154148/156825180043216_en-US.png)

4.  Enter a search and analysis statement, select a time range, and click **Search & Analysis**.

    ![查询分析](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/154148/156825180043218_en-US.png)


## More actions

On the **Log Analysis** page, you can perform the following actions to handle the returned search results:

-   **Customize search and analysis**

    The log analysis function provides the search and analysis statements for you to search and analyze log entries in different scenarios. For more information, see [Customize search and analysis](#section_ncn_mvt_j2b).

-   **View the distribution of log entries by time**

    The histogram under the search box shows the distribution of log entries that are filtered by time and search statement. The horizontal axis indicates the time period, and the vertical axis indicates the number of log entries. The total number of the log entries returned is also displayed.

    **Note:** You can drag the mouse pointer in the histogram to narrow down the time period. The `time picker` automatically updates the time period, and the search results are also updated accordingly.

    ![时间分布](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/154148/156825180043220_en-US.png)

-   **View raw logs**

    On the **Raw Logs** tab page, each log entry is detailed on an individual page, which includes the time when the log is generated, the content, and the columns in the log entry. You can click **Display Content Column** to set the display mode for the long strings in the content column. The display modes include **Full Line** and **New Line**. You can click **Column Settings** to customize the columns to be displayed, or click the Download icon to download the search results.

    ![原始日志](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/154148/156825180043221_en-US.png)

    Additionally, you can click a value or a property name in the content column to add a search condition to the search box. For example, if you click `log_service` in the `__source__: log_service` field, the following search statement is added to the search box:

    ```
    "Former Search Statement" and source: log_service
    ```

-   **View analysis graphs**

    The log analysis function enables you to show the analysis results in graphs. You can select the graph type as needed on the Graph tab page. For more information, see [Analysis graphs](/intl.en-US/Query and visualization/Analysis graph/Overview.md).

    ![统计图表](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/154148/156825180143222_en-US.png)

-   **Quick analysis**

    The quick analysis function on the Raw Logs tab provides you with a quick interactive search function. You can view the distribution of a property within a specific time period. This function can reduce the time used for indexing key data. For more information, see [Quick analysis](/intl.en-US/Index and query/Query/Quick analysis.md).

    ![快速分析](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/154148/156825180143223_en-US.png)


## Customize search and analysis

The log analysis function provides the search and analysis statements. Separate the search and analysis statements with a vertical bar \(`|`\):

```
$Search | $Analytics
```

|Type|Description|
|:---|:----------|
|Search|A keyword, a fuzzy string, a numerical value, or a range can be used as a search condition. You can also combine these search conditions. If the statement is empty or only contains a wildcard character \(`*`\), all log entries are searched.|
|Analytics|Performs calculation and statistics to the search results or all log entries.|

**Note:** Both the search and the analysis statements are optional.

-   When the search statement is empty, all log entries within the specified time period are displayed. Then, the search results are used for statistics.
-   When the analysis statement is empty, the search results are returned. No statistical analysis is performed.

**Search statements**

The search statements of Log Service support **full text search** and **field search**. You can set the New Line mode, syntax highlighting, and other functions in the search box.

-   **Full text search**

    You can enter keywords without specifying fields to perform the search. You can enter a keyword enclosed in quotation marks \("\) to query log entries that contain the entire keyword. You can also use spaces or `and` to separate multiple keywords.

    **Examples**

    -   **Search by keyword**

        The following statements can be used to search for log entries that contain `www.aliyun.com` and `error`.

        `www.aliyun.com error` or `www.aliyun.com and error`.

    -   **Search by condition**

        The following statement can be used to search for log entries that contain `www.aliyun.com`, `error`, or `404`.

        ```
        www.aliyun.com and (error or 404)
        ```

    -   **Search by prefix**

        The following statement can be used to search for log entries that contain `www.aliyun.com` and start with `failed_`.

        ```
        www.aliyun.com and failed_*
        ```

        **Note:** The wildcard character \(`*`\) can only be added as a suffix. The wildcard character \(`*`\) cannot be added as a prefix. For example, the statement cannot be `*_error`.

-   **Search by field**

    To narrow down the search results, you can search by field.

    You can specify numeric fields. The format is `field name: value` or `field name>=value`. Moreover, you can use both the `and` and `or` operators in full text search.

    **Note:** The Cloud Firewall log analysis function supports searching by field. For more information about the definition, type, format, and other information of each field, see [Cloud Firewall log field descriptions](/intl.en-US/Log Management/Log service/Log fields.md).

    **Examples**

    -   **Search by specifying multiple fields**

        If you want to search for log entries about client `1.2.3.4` accessing IP address `1.1.1.1`, set the following search conditions:

        ```
        src_ip: 1.2.3.4 and dst_ip: 1.1.1.1
        ```

        **Note:** In this example, the `src_ip` field and `dst_ip` field are log fields created by Cloud Firewall.

    -   **Search by specifying numeric fields**

        The following statement can be used to search log entries where the response time exceeds five seconds.

        ```
        request_time_msec > 5000
        ```

        Searching by time period is also supported. For example, you can search for log entries where the response time exceeds five seconds and is no greater than ten seconds.

        ```
        request_time_msec in (5000 10000]
        ```

        **Note:** You can get the same result by using the following search statement:

        ```
        request_time_msec > 5000 and request_time_msec <= 10000
        ```

    -   **Field search**

        You can search whether a field exists as follows:

        -   Search for log entries that include the `total_pps` field.

            ```
            total_pps :*
            ```

        -   Search for log entries that include the `ua_browser` field .

            ```
            not total_pps :*
            ```


For more information about the search statements supported by Log Service, see [Indexes and search](/intl.en-US/Index and query/Overview.md).

**Analysis statements**

You can use the SQL/92 statements for log analysis and statistics.

For more information about the statements and functions supported by Log Service, see [Real-time analysis](/intl.en-US/Index and query/Real-time log analysis.md).

**Note:**

-   The `from table name` part \(the `from log` part\) in the standard SQL statements can be omitted.
-   The first 100 log entries are returned by default. You can modify the number of the returned log entries by using the [LIMIT statement](/intl.en-US/Index and query/Analysis grammar/LIMIT syntax.md).

## Examples of search and analysis

**Time-based log search and analysis**

Each Could Firewall log entry has a `time` field, which is used to indicate the time. The format of field is `year-month-dayThour:minute:second+time zone`. For example, in `2018-05-31T20:11:58+08:00`, the time zone is `UTC+8`.

Meanwhile, each log has a built-in field `__time__`, This field also indicates the time when the log entry is generated. The field is used for calculation during the time-based statistics process. The format of this field is Unix timestamp, and the value of this field indicates the amount of seconds that have elapsed since 00:00:00 Coordinated Universal Time \(UTC\), January 1, 1970. Therefore, if you want to display a calculated result, you must convert the format first.

-   **Select and display the time**
-   **Calculate the time**
-   **Statistical analysis by group based on a specific time**

    **Note:** You can also display the results with a line graph.

    ![折线](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3317436851/p43231.png)


The `date_parse` and `date_format` functions are used to convert the time format. For more information about the functions that can be used to parse the time field, see [Date and time functions](/intl.en-US/Index and query/Analysis grammar/Date and time functions.md).

