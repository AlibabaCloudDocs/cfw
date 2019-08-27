# Create application groups and business groups {#concept_337351 .concept}

Cloud Firewall visualizes the traffic between businesses to help you learn about the access relationships between businesses and choose access control policies to be applied.

To visualize the traffic, you must create business groups and application groups and add applications to these groups.

## Background information {#section_rw9_ep2_5j6 .section}

Make sure that you understand the following basic concepts:

-   **Business group**: In east-west traffic visualization, a business group is a set of application groups that provide the same service or similar services. For example, a Web portal business group contains Web application groups and database application groups.
-   **Application group**: In east-west traffic visualization, an application group is a set of applications that provide the same service or similar services. For example, all ECS instances deployed with MySQL can be added to one database application group.
-   **Application**: The smallest unit in east-west traffic visualization. An application is a set of all open ports on an ECS instance by default. You can create a new application by cloning the default application through a specified port.

## Step 1: Create a business group {#section_iwt_cr9_t31 .section}

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the left-side navigation pane, choose **Business Visualization** \> **Application Groups** \> **Business Groups**.
3.  In the upper-left corner of the Business Groups tab page, select a VPC network for the business group to be created.

    **Note:** You can select from existing VPC networks and Classic networks. You must specify only one VPC network for each business group.

4.  In the upper-right corner, click **Create Business Group**.
5.  In the Create Business Group dialog box, configure the business group information.
    -   **Name**: Enter the business group name. The name must be from 1 to 40 characters in length.
    -   **Description**: Enter the business group description.
    -   **Importance Degree**: Specify the importance degree of the business group. This helps you distinguish business groups of different importance degrees in the business relations graph. The importance degrees include moderate, important, and critical.

        On the Business Relations page, you can view business groups of specified importance degrees.

6.  Click **OK**.

    The new business group belongs to the VPC network that you selected. In the business group list, you can **modify** or **delete** business groups.

    **Note:** You cannot delete a business group that contains application groups.


## Step 2: Create an application group {#section_5vs_9n3_po4 .section}

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the left-side navigation pane, choose **Business Visualization** \> **Application Groups** \> **Application Groups**.
3.  In the upper-left corner of the Application Groups tab page, select a VPC network for the application group to be created.
4.  In the upper-right corner, click **Create Application Group**.
5.  In the Create Application Group dialog box, configure the application group information.
    -   **Name**: Enter the application group name. The name must be from 1 to 40 characters in length.
    -   **Description**: Enter the application group description.
    -   **Importance Degree**: Specify the importance degree of the application group. This helps you distinguish application groups of different importance degrees in the business relations graph. The importance degrees include moderate, important, and critical.

        On the Business Relations page, you can click a business group, and view applications groups of specified importance degrees.

    -   **Business Group**: You can select an existing business group or create a business group.
        -   If you choose to select an existing business group, select a business group in the **Name** drop-down list.

            **Note:** The new application group is automatically added to the VPC network that the specified business group belongs to.

        -   If you choose to create a business group, specify the **name**, **description**, and **importance degree** of the new business group.
6.  Click **OK**.
7.  \(Optional\) You can click **Assign** in the **Actions** column to change the business group that an application group belongs to. After this operation, the data in the **Application Groups** column on the Business Groups tab page is changed.

    You can also **modify** or **delete** the application groups.

    **Note:** You cannot delete an application group that contains applications.


## Step 3: Specify an application group and a business group for an application {#section_1q4_rtf_5py .section}

On the Applications tab page, you can view the numbers of business groups, application groups, applications, and ECS instances in Cloud Firewall.

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the left-side navigation pane, choose **Business Visualization** \> **Application Groups** \> **Applications**.
3.  Search for a specific application.
4.  Click **Assign** in the **Actions** column. In the dialog box that appears, select the business group and application group that you created.

    **Note:** After this operation, the numbers of **business groups** and **application groups** on the Business Groups tab page are changed.

5.  \(Optional\) You can also click **Clone** in the **Actions** column to create a new application based on the specified application.

    After you activate Cloud Firewall, a default application is created for each ECS instance. The traffic bound to an ECS instance is automatically associated with the default application. If the applications on an ECS instance are associated with different businesses, you can use the **clone** operations to create a new application and assign **another business group and another application group**. When you clone an application, you can modify the ECS instance ID, **listening port**, and **process name**.


## Subsequent operations {#section_lmu_4ts_gj8 .section}

View the business relations graph.

