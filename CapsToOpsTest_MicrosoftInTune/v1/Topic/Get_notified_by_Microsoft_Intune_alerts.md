---
description: na
search: na
title: Get%20notified%20by%20Microsoft%20Intune%20alerts
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.date: 2015-09-14
ms.author: 03258b9b-2cea-4654-ab05-a27214174f4b
---
# Get%20notified%20by%20Microsoft%20Intune%20alerts
Alerts keep you in touch with what's happening in [!INC[wit_firstref](../Token/wit_firstref_md.md)].

For example, alerts can notify you about the following events:

- A problem with the Exchange Connector which affects mobile device management

- Malware has been found on a computer

- A conflict between two [!INC[wit_nextref](../Token/wit_nextref_md.md)] policies was detected

- The latest updates and information about the [!INC[wit_nextref](../Token/wit_nextref_md.md)] service (notices).

## How alerts work
Alerts are generated based on **alert types**, a set of preconfigured rules built into [!INC[wit_nextref](../Token/wit_nextref_md.md)]. For example, the alert type **Cloud storage has 10% or less free space** alerts you when you are running out of space to store your apps in the cloud. You can enable or disable, and configure properties for each alert type. For example, using the above alert type, you can configure:

- **State:** Whether this alert type is enabled or disabled

- **Severity:** How serious is this alert?

   |||
   |-|-|
   |Severity <br /> <br />|Description <br /> <br />|
   |![](../Image/Critical_Alert.jpg) <br /> <br />|Indicates a serious issue that you should investigate as soon as possible, for example, if malware has been detected on a computer. <br /> <br />|
   |![](../Image/Warning_Alert.jpg) <br /> <br />|Indicates an issue that isn't currently serious, but might become serious if you don't attend to it, for example, security updates are waiting to be installed. <br /> <br />|
   |![](../Image/Informational_Alert.jpg) <br /> <br />|Indicates information that isn't critical to your operations, for example, a new version of the Exchange Connector is available. <br /> <br />|

Other alert types might contain different items you can configure such as the percentage of devices that must be affected by an issue before an alert is generated.

**When the criteria in an alert type is met, an alert is generated and displayed in the [!INC[wit_nextref](../Token/wit_nextref_md.md)] admin console.**

Additionally, you can configure [!INC[wit_nextref](../Token/wit_nextref_md.md)] to notify you by email when an alert is generated.

## Configuring alerts
In the [Microsoft Intune administration console](https://manage.microsoft.com), click **Admin** &gt; **Alerts and Notifications**, then choose one of the following configuration tasks:

|Task <br /> <br />|Description <br /> <br />|
|--------|---------------|
|**Alert Types** <br /> <br />|Choose the alert type you want to configure, then do one of the following: <br /> <br /><ul><li>Click **Configure**. In the **Configure Alert Type** dialog box, configure the settings you want, then click **OK**. </li><li>**Enable** or **Disable** the alert. </li> </ul> **Tip:** Expand the **Alert Types** node and click a category to view only the alert types in that category. <br />|
|**Recipients** <br /> <br />|Click **Add** to add a new email address that will receive the email notifications you configure. <br /> <br />You can also **Edit** or **Delete** existing recipients. **Tip:** To receive notifications, you must also add this email address as a recipient under **Notification Rules**. <br />|
|**Notification Rules** <br /> <br />|Configures rules that define who an email alert will be sent to. You can either: <br /> <br /><ul><li>**Choose an existing rule** - Choose a rule, then click **Select Recipients**. You can then select all recipients who will receive an email when an alert that fulfills this rule is generated. </li><li>**Create a new rule** - Click **Create New Rule**, then: <br /> <br /><ol><li>Enter a name for the rule, then select the alert categories and alert severity that apply to the rule. </li><li>Select the device groups that the rule applies to. </li><li>Select the users who will receive an email when an alert is generated. </li> </ol> </li><li>Click **Save**. </li> </ul>You can also **Enable**, **Disable**, **Edit**, or **Delete** an existing rule. <br /> <br />|

## Working with alerts
Use the following options to help you work with alerts from the Intune admin console.

|Option <br /> <br />|Description <br /> <br />|
|----------|---------------|
|View active alerts <br /> <br />|Choose one of: <br /> <br /><ul><li>**View an alert summary** - In the **Dashboard** workspace, the top errors are displayed in the Alerts pane. Click the pane to see more detailed information. <br /> <br />   Additionally, you can view an alert summary on the **Overview** page of the **Alerts** workspace. </li><li>**View all alerts** - In the **Alerts** workspace, click **All Alerts**. </li> </ul>|
|View notices <br /> <br />|Choose one of: <br /> <br /><ul><li>In the **Dashboard** workspace, click **Notices**. </li><li>In the **Alerts** workspace, click **All Alerts** &gt; **Notices**. </li> </ul>|
|Close an alert <br /> <br />|In the list of alerts, choose the alert to close, then click **Close Alert**. <br /> <br />Closed alerts are permanently deleted after 90 days. <br /> <br />|
|Reactivate a closed alert <br /> <br />|In the list of alerts, set the **Filters** drop-down to **Closed**. <br /> <br />In the list of closed alerts, select the alert you want to reactivate, then click **Reactivate Alert**. <br /> <br />|
[!INC[wit_nextref](../Token/wit_nextref_md.md)] alerts remain active until:

- The issue that caused the alert is resolved

- You manually close the alert

- 45 days have passed since the alert was generated

> [!TIP]
> If the same alert is generated by devices that run different operating systems, you might see multiple versions of the same alert in the alerts list.

## See Also
[Monitoring and reports with Microsoft Intune](../Topic/Monitoring_and_reports_with_Microsoft_Intune.md)

