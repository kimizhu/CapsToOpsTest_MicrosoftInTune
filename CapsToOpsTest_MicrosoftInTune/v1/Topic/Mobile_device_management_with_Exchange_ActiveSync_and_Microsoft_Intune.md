---
description: na
search: na
title: Mobile device management with Exchange ActiveSync and Microsoft Intune
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.date: 2015-10-22
ms.author: f93f38ed286b4cbb94b9b427a0abc63e
capscontentguid: eb9618d2-dc90-48be-b921-8044b7e693ac
---
# Mobile device management with Exchange ActiveSync and Microsoft Intune
For [!INC[wit_nextref](../Token/wit_nextref_md.md)] to directly manage mobile devices, users need to enroll devices into [!INC[wit_nextref](../Token/wit_nextref_md.md)]. For mobile devices that users have not enrolled you can enable Exchange ActiveSync management using the Exchange connector. Exchange devices can be managed in both on premises servers and for hosted Exchange on Microsoft Office 365 in the cloud. The Exchange connector connects you with your Exchange deployment and lets you manage mobile devices through the [!INC[wit_nextref](../Token/wit_nextref_md.md)] console, where you have the following capabilities:

- Deploy policies to user groups to help secure corporate data that is stored on mobile devices such as password, encryption, and attachments.

- Define mobile device access rules by device family and device model to set which mobile devices can access Exchange ActiveSync.

- Enroll, rename, and un-enroll devices.

- Wipe mobile devices with the option to wipe the mobile device, such as for lost or stolen devices.

This topic contains the following sections:

- [Configure Microsoft Intune on-premises connector for on-premises or hosted Exchange](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md#bkmk_EX_OP): Use this section to configure your on-premises infrastructure with on-premises Exchange or hosted Exchange.

- [Configure Microsoft Intune service to service connector for hosted Exchange](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md#bkmk_S_S)

- [Validate your Exchange connection](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md#bkmk_val_ex)

- [Wipe for Exchange-managed mobile devices](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md#bkmk_EXCap)

- [Policy for Exchange-managed mobile devices](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md#bkmk_pol)

- [Exchange Access rules for mobile devices](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md#bkmk_acc)

## <a name="bkmk_EX_OP"></a>Configure Microsoft Intune on-premises connector for on-premises or hosted Exchange
Use this section to configure your on-premises infrastructure with on-premises Exchange or hosted Exchange.

### Requirements
To prepare to connect [!INC[wit_nextref](../Token/wit_nextref_md.md)] to your Exchange Server, you must first fulfill the following requirements. You may have already fulfilled these requirements when you set up [!INC[wit_nextref](../Token/wit_nextref_md.md)].

|Requirement <br /> <br />|More information <br /> <br />|
|---------------|--------------------|
|Set the Mobile Device Management Authority to [!INC[wit_nextref](../Token/wit_nextref_md.md)] <br /> <br />|[Set mobile device management authority as Microsoft Intune](../Topic/Set_mobile_device_management_authority_as_Microsoft_Intune.md) <br /> <br />|
|Verify you have hardware requirements for the on-premises connector <br /> <br />|[Requirements for the On-Premises Exchange Connector](../Topic/Network_infrastructure_requirements_for_Microsoft_Intune.md#BKMK_ExchanceConnectorReqs) <br /> <br />|
|Configure a user account with permission to run the designated list of Windows PowerShell cmdlets <br /> <br />|Powershell Cmdlets for On-Premises Exchange Connector (see below) <br /> <br />|

### <a name="bkmk_PS_onprem"></a>Powershell Cmdlets for On-Premises Exchange Connector
You must create an Active Directory user account that is used by the [!INC[wit_nextref](../Token/wit_nextref_md.md)] Exchange Connector. The account must have permission to run the following required Windows PowerShell Exchange cmdlets:

- Get-ActiveSyncOrganizationSettings, Set-ActiveSyncOrganizationSettings

- Get-CasMailbox, Set-CasMailbox

- Get-ActiveSyncMailboxPolicy, Set-ActiveSyncMailboxPolicy, New-ActiveSyncMailboxPolicy, Remove-ActiveSyncMailboxPolicy

- Get-ActiveSyncDeviceAccessRule, Set-ActiveSyncDeviceAccessRule, New-ActiveSyncDeviceAccessRule, Remove-ActiveSyncDeviceAccessRule

- Get-ActiveSyncDeviceStatistics

- Get-ActiveSyncDevice

- Get-ExchangeServer

- Get-ActiveSyncDeviceClass

- Get-Recipient

- Clear-ActiveSyncDevice, Remove-ActiveSyncDevice

- Set-ADServerSettings

- Get-Command

### Download, Install and Configure the Microsoft Intune Exchange Connector
To set up a connection that enables [!INC[wit_nextref](../Token/wit_nextref_md.md)] to communicate with the Exchange Server that hosts the mobile devices’ mailboxes, you must download and configure the On-Premises Connector tool from the [!INC[wit_nextref](../Token/wit_nextref_md.md)] administrator console.

##### To download the On-Premises Connector software installation package

1. Open the [!INC[wit_adminconsole](../Token/wit_adminconsole_md.md)].

2. In the workspace shortcuts pane, click **Administration**.

3. In the navigation pane, under **Mobile Device Management**, expand **Microsoft Exchange** and then click **Setup Exchange Connection**.

4. On the **Setup Exchange Connection** page, click **Download On-Premises Connector**.

5. The On-Premises Connector software is contained in a compressed (.zip) folder that can be opened or saved. In the **File Download** dialog box, click **Save** to store the compressed folder to a secure location.

> [!IMPORTANT]
> Do not rename or move the extracted files or the On-Premises Connector software installation will not succeed.

Perform the following steps to install the [!INC[wit_nextref](../Token/wit_nextref_md.md)] On-Premises Connector.

> [!IMPORTANT]
> The On-Premises Connector can only be installed once per [!INC[wit_nextref](../Token/wit_nextref_md.md)] subscription, and only on one computer. If you attempt to install the On-Premises Connector a second time, you will replace the initial Exchange connection.

##### To install the On-Premises Connector

1. Extract the files in **Exchange_Connector_Setup.zip** into a secure location.

2. After the files are extracted, double-click **Exchange_Connector_Setup.exe** to install the On-Premises Connector.

   > [!IMPORTANT]
   > If the destination folder is not a secure location, you should delete the certificate file **WindowsIntune.accountcert** after you install the On-Premises Connector.

> [!NOTE]
> You can only set up one Exchange connection per [!INC[wit_nextref](../Token/wit_nextref_md.md)] account. If you try to configure an additional connection, it will replace the original connection with the new one.

##### Configure the On-Premises Exchange Connector

1. In the **Exchange server** field, select your Exchange server environment type, either **On-premises Exchange Server** or select **Hosted Exchange Server** for Exchange on Microsoft Office 365.

2. For an on-premises Exchange server, provide either the server name or fully qualified domain name of the Exchange server that hosts the Client Access server role.

3. For a hosted Exchange server in Microsoft Office 365, provide the Exchange server address.  To find the hosted Exchange server URL:

   1. Open the Outlook Web App for Office 365.

   2. Click the “?” icon at the top left, and select **About**.

   3. Locate the **POP External Server** value.

4. For a dedicated, hosted Exchange server, provide either the server name or the fully qualified domain name of the dedicated Exchange server that hosts the Client Access server role.

5. Click **Proxy Server** to specify proxy server settings for your hosted Exchange server.

   1. Select **Use a proxy server when synchronizing mobile device information**.

   2. Enter the **proxy server name** and the **port number** to be used to access the server.

   3. If it is necessary to provide user credentials to access the proxy server, select Use credentials to connect to the proxy server and enter the **domain\user** and the **password**.

   4. Click **OK**.

6. Provide the credentials necessary to connect to your Exchange server.

7. Provide administrative credentials necessary to send notifications to a user’s Exchange mailbox. These notifications are configurable via Conditional Access policies using Intune. For more information on these policies see [Enable access to company resources with Microsoft Intune](http://msdn.microsoft.com/en-us/library/5b090c5a-6f12-4e60-ace0-c9929afaa9a3).

   Ensure that the Autodiscover service and Exchange Web Services are configured on the Exchange Client Access Server. For more information on that see [Client Access server](https://technet.microsoft.com/library/dd298114.aspx).

8. In the **Password** field, provide the password for this account to enable [!INC[wit_nextref](../Token/wit_nextref_md.md)] to access the Exchange Server.

9. Click **Connect**.

   It may take a few minutes while the connection is set up.

   During configuration, the [!INC[wit_exch_2](../Token/wit_exch_2_md.md)] stores your proxy settings to enable access to the Internet. If your proxy settings change, you will have to reconfigure the [!INC[wit_exch_2](../Token/wit_exch_2_md.md)] in order to apply the updated proxy settings to the [!INC[wit_exch_2](../Token/wit_exch_2_md.md)].

After the [!INC[wit_exch_2](../Token/wit_exch_2_md.md)] sets up the connection, mobile devices associated with users that are managed in [!INC[wit_nextref](../Token/wit_nextref_md.md)] are automatically synchronized and added to the [!INC[wit_adminconsole](../Token/wit_adminconsole_md.md)]. This synchronization may take some time to complete.

To view the status of the connection and the last successful synchronization attempt, in the [!INC[wit_adminconsole](../Token/wit_adminconsole_md.md)] click the **Administration** workspace, and under **Mobile Device Management**, click **Exchange**.

> [!NOTE]
> If you have installed the On-Premises Connector, and if at some point you delete the Exchange connection, you must uninstall the On-Premises Connector from the computer onto which it was installed.

## <a name="bkmk_S_S"></a>Configure Intune service to service connector for hosted Exchange
Use this section to connect [!INC[wit_firstref](../Token/wit_firstref_md.md)] and hosted Exchange without an on-premises infrastructure.

### Requirements
To prepare to connect [!INC[wit_nextref](../Token/wit_nextref_md.md)] to your Exchange Server, make sure you have completed the following:

|Requirement <br /> <br />|More information <br /> <br />|
|---------------|--------------------|
|Set the Mobile Device Management Authority to [!INC[wit_nextref](../Token/wit_nextref_md.md)] <br /> <br />|[Get ready to enroll devices in Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md) <br /> <br />|
|Verify you have hardware requirements for the on-premises connector <br /> <br />|[Requirements for the Service to Service Connector](../Topic/Network_infrastructure_requirements_for_Microsoft_Intune.md#BKMK_ServiceConnectorReqs) <br /> <br />|
|Configure a user account with permission to run the designated list of Windows PowerShell cmdlets <br /> <br />|PowerShell Cmdlets for Service to Service Connector (See below) <br /> <br />|

### <a name="Bkmk_PS_STS"></a>PowerShell Cmdlets for Service to Service Connector
You must create an Exchange Online user account that is used by the [!INC[wit_nextref](../Token/wit_nextref_md.md)] Exchange Connector. The account must have permission to run the required Windows PowerShell Exchange cmdlets that are listed below.

- Get-ActiveSyncOrganizationSettings, Set-ActiveSyncOrganizationSettings

- Get-MobileDeviceMailboxPolicy, Set-MobileDeviceMailboxPolicy, New-MobileDeviceMailboxPolicy, Remove-MobileDeviceMailboxPolicy

- Get-ActiveSyncDeviceAccessRule, Set-ActiveSyncDeviceAccessRule, New-ActiveSyncDeviceAccessRule, Remove-ActiveSyncDeviceAccessRule

- Get-MobileDeviceStatistics

- Get-MobileDevice

- Get-ActiveSyncDeviceClass

- Get-Recipient

- Clear-MobileDevice, Remove-MobileDevice

### Set up the Service to Service Connector

1. Open the [!INC[wit_adminconsole](../Token/wit_adminconsole_md.md)].

2. In the workspace shortcuts pane, click **Administration**.

3. In the navigation pane, under **Mobile Device Management**, expand **Microsoft Exchange** and then click **Set Up Exchange Connection**.

4. On the **Set Up Exchange Connection** page, click **Set Up Service to Service Connector**.

The Service to Service Connector will automatically configure and synchronize with your Hosted Exchange environment.

## <a name="bkmk_val_ex"></a>Validate your Exchange connection

- After you have successfully configured the [!INC[wit_exch_2](../Token/wit_exch_2_md.md)], in the [!INC[wit_adminconsole](../Token/wit_adminconsole_md.md)] click the **Administration** workspace, and under **Mobile Device Management**, click **Microsoft Exchange** and validate that the details you provided appear under **Exchange Connection Information**.

- You can also check the time and date of the last successful synchronization attempt.

## <a name="bkmk_EXCap"></a>Wipe for Exchange-managed Mobile Devices
The following table describes the retire/wipe capabilities through Exchange ActiveSync.

|Type of Wipe <br /> <br />|Windows 8.1 and Windows RT 8.1 <br /> <br />|Windows RT <br /> <br />|Windows Phone 8 <br /> <br />|iOS <br /> <br />|Android <br /> <br />|
|----------------|----------------------------------|--------------|-------------------|-------|-----------|
|Full Wipe <br /> <br />|Removes mail account and cached mail. <br /> <br />|Removes mail account and cached mail. <br /> <br />|Factory Reset <br /> <br />|Factory Reset <br /> <br />|Factory Reset <br /> <br />|
|Selective Wipe/Email <br /> <br />|Removes email account <br /> <br />|Removes email account <br /> <br />|Not supported. <br /> <br />|Not supported. <br /> <br />|Not supported. <br /> <br />|
|Selective Wipe/policies <br /> <br />|Policy enforcement removed, but settings are not changed <br /> <br />|Policy enforcement removed, but settings are not changed <br /> <br />|Policy enforcement removed, but settings are not changed <br /> <br />|Policy enforcement removed, but  settings are not changed <br /> <br />|Policy enforcement removed, but settings are not changed <br /> <br />|

## <a name="bkmk_pol"></a>Policy for Exchange-managed mobile devices
Policy settings can be applied through the [!INC[wit_nextref](../Token/wit_nextref_md.md)] console, see [Manage settings and features on your devices with Microsoft Intune policies](../Topic/Manage_settings_and_features_on_your_devices_with_Microsoft_Intune_policies.md). For a detailed list of Exchange ActiveSync policy settings and features that are supported by specific mobile devices, see [Exchange ActiveSync Client Comparison Table](http://go.microsoft.com/fwlink/?LinkId=247270).

> [!NOTE]
> Upon connecting [!INC[wit_nextref](../Token/wit_nextref_md.md)] to a Microsoft Exchange environment, all users managed through [!INC[wit_nextref](../Token/wit_nextref_md.md)] will have their EAS policy reset to the current default policy on the Microsoft Exchange server, unless there is a more specific policy defined within [!INC[wit_nextref](../Token/wit_nextref_md.md)].

## <a name="bkmk_acc"></a>Exchange Access rules for mobile devices
Exchange access rules for mobile devices determine the level of access to Exchange that is granted to mobile devices. These setting will affect all mobile devices, even the mobile devices not enrolled in [!INC[wit_nextref](../Token/wit_nextref_md.md)]. You can start off by defining a **Default Rule** which will apply to any mobile device that does not have a custom rule applied to it. The following table contains the access levels managed by Exchange ActiveSync:

|Access level <br /> <br />|Description <br /> <br />|
|----------------|---------------|
|**Allow all mobile devices to access Exchange, unless a custom rule states otherwise** <br /> <br />|In the allow access state, a mobile device can synchronize through Exchange ActiveSync and connect to the Exchange server to retrieve email and manipulate calendar information, contacts, tasks, and notes. This will continue as long as the device complies with the [!INC[wit_nextref](../Token/wit_nextref_md.md)]**Mobile Device Security Policy** that you have configured, unless the user or the specific mobile device has been blocked by the Exchange administrator. <br /> <br />|
|**Block all mobile devices from accessing Exchange, unless a custom rule states otherwise** <br /> <br />|A mobile device that is blocked because of a device access setting you configured will not be allowed to connect to the Exchange server and will receive HTTP 403 Forbidden errors. The user will receive an email message from the Exchange server telling them that the mobile device was blocked from accessing their mailbox. The user will not be able to read the email message on the blocked mobile device. You can add customized text to this message to provide instructions for users whose devices are blocked through the **Set User Notification** task. <br /> <br />|
|**Quarantine all mobile devices so I can decide later for each individual mobile device, unless a custom rule states otherwise** <br /> <br />|When a mobile device is quarantined, the mobile device is allowed to connect to the Exchange server. However, it is given only limited access to data. The user can add content to their own Calendar, Contacts, Tasks, and Notes folders but the server will not allow the device to retrieve any content from the user's mailbox. The user will receive a single email message that tells them that the mobile device is quarantined. This message will be received by the device and will also be available in the user's mailbox. You can add customized text to this message to provide instructions for users whose devices are quarantined through the **Set User Notification** task. <br /> <br />|
An access strategy is a combination of a **Default Rule** and **Custom Rules** that apply to all mobile devices connected to exchange. The table below lists some example access strategies.

|Access Strategy <br /> <br />|Description <br /> <br />|
|-------------------|---------------|
|Allow list <br /> <br />|You can use an allow list to grant access to a list of known devices and restrict access for everything else. To do this, you must create custom rules so that the specific devices you want are allowed to access users' mailboxes. As soon as you create such a rule, you must set the default access rule to block or quarantine all other devices. To add a new device to the allow list, create a new custom rule <br /> <br />|
|Block list <br /> <br />|You can use a block list to grant access to all devices by default, but to block access for a set of devices that you do not want to access your organization. You create a block list by creating custom rules to block the devices that you do not want to synchronize with the organization’s mailboxes. The default rule should be set to allow access to all devices that are not explicitly blocked by the existing rules. To add a new device or set of devices to the block list, create a new custom rule. <br /> <br />|
|Mixed allow and block <br /> <br />|In addition to creating allow and block lists, you can quarantine new mobile devices as they are introduced into the organization while you evaluate them. For example, if you have a block list for mobile devices that are not allowed within your organization, and an allow list for mobile devices that are allowed within the organization, you can set the default rule to quarantine. All other devices will automatically be quarantined, which lets you discover new devices as they are introduced to the organization and decide whether to add them to the allow list or the block list. <br /> <br />|
The following procedure describes how to create a custom rule.

#### Create a Default Access Rule

1. Open the [!INC[wit_adminconsole](../Token/wit_adminconsole_md.md)].

2. In the workspace shortcuts pane, click the **Policy** icon and click **Exchange Access for Mobile Devices**.

3. In the **Default Rule** list, select the Access Rule that you wish to apply to all mobile devices not covered by a rule or personal exemption. Click **Save**.

The following procedure describes how to create a custom rule.

#### Create a Custom Access Rule

1. Open the [!INC[wit_adminconsole](../Token/wit_adminconsole_md.md)].

2. In the workspace shortcuts pane, click the **Policy** icon and click **Exchange Access for Mobile Devices**.

3. In the **Custom Rules** list, Click **Add Rule** and create a custom rule. Click **Save**.

## See Also
[Get ready to enroll devices in Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md)

