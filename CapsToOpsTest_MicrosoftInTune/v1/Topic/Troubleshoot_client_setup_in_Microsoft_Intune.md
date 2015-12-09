---
description: na
search: na
title: Troubleshoot client setup in Microsoft Intune
ms.service: na
ms.tgt_pltfrm: na
ms.topic: article
ms.date: 2015-10-15
ms.author: 03258b9b-2cea-4654-ab05-a27214174f4b
---
# Troubleshoot client setup in Microsoft Intune

## Troubleshooting client set up problems
Use the following sections to help you troubleshoot common client setup problems.

### What to do if client installation fails

- If no client software deployment alerts for the computer are displayed in the [!INC[wit_adminconsole](../Token/wit_adminconsole_md.md)], check the computer’s Internet connectivity and proxy configuration and make sure that the computer can communicate with the service URL, [https://manage.microsoft.com](https://manage.microsoft.com). Then retry the client software installation.

- You can have an email sent to selected recipients when a client software deployment failure alert occurs by configuring a notification rule in the **Admin** workspace. For more information, see [Get notified by Microsoft Intune alerts](../Topic/Get_notified_by_Microsoft_Intune_alerts.md).

- [!INC[wit_firstref](../Token/wit_firstref_md.md)] displays the critical alert **Client Software Deployment Failure** if the client software fails to deploy. This will display in the **System Overview** page and **Alerts** pages of the [!INC[wit_adminconsole](../Token/wit_adminconsole_md.md)]. Check for alerts by using the following procedure:

##### To check alerts for failed installations

1. In the [Microsoft Intune administration console](https://manage.microsoft.com/), click **Alerts** &gt; **Overview**.

2. On the **Alerts overview** page, you can review the following information:

   - The top three alerts, which can be sorted by date, category, or severity

   - The total number of active alerts

3. Click **All Alerts** to display the following information on the **Alerts** page. Critical alerts are displayed first:

   - **Name** – The name of the alert type that generated the alert.

   - **Source** – A link to the source of the alert.  If the display threshold of the alert type is set to **All**, then this link will display a single affected device.  If the display threshold of the alert type is set to a value, then this link will display a list of all the devices that are affected by this alert.

   - **Last Updated** – This indicates the time when the alert was last modified. If an alert is closed, the time when the alert was closed is displayed.

   - **Severity** – This indicates the severity of the alert

### <a name="BKMK_Whattodo"></a>What to do if the client will not uninstall from the Microsoft Intune administrator console

##### To remove the client software by using the Microsoft Intune command line tool

1. Open a command prompt in administrator mode.

2. Go to the folder *%programfiles%\Microsoft\OnlineManagement\Common*

3. Run the following command - **ProvisioningUtil.exe /UninstallAgents /MicrosoftIntune**

### Client installation error codes
The following table describes error codes that are displayed in **Alerts** if client software installation fails. It includes suggestions for resolving the problem that is represented by each error code.

|Error code <br /> <br />|Possible problem <br /> <br />|Suggested resolution <br /> <br />|
|--------------|--------------------|------------------------|
|**0x80CF0437** <br /> <br />|The clock on the client computer is not set to the correct time. <br /> <br />|Make sure that the clock and the time zone on the client computer are set to the correct time and time zone. <br /> <br />|
|**0x80240438**, **0x80CF0438**, **0x80CF401B** <br /> <br />|Cannot connect to the [!INC[wit_firstref](../Token/wit_firstref_md.md)] service. Check the client proxy settings. <br /> <br />|Verify that the proxy configuration on the client computer is supported by [!INC[wit_firstref](../Token/wit_firstref_md.md)], and that the client computer has Internet access. For more information about supported proxy configurations, see [Help secure Windows PCs with Endpoint Protection for Microsoft Intune](../Topic/Help_secure_Windows_PCs_with_Endpoint_Protection_for_Microsoft_Intune.md). <br /> <br />|
|**0x80CF402C** <br /> <br />|Cannot connect to the [!INC[wit_firstref](../Token/wit_firstref_md.md)] service. Check network connectivity. <br /> <br />|Verify the computer has network connectivity. Ensure the network cable is connected or wireless network in on. <br /> <br />|
|**0x80240438, 0x80CF0438** <br /> <br />|Proxy settings in Internet Explorer and Local System are not configured. <br /> <br />|Check the client proxy settings and confirm that the proxy configuration on the client computer is supported by [!INC[wit_firstref](../Token/wit_firstref_md.md)], and that the client computer has Internet access. For more information about supported proxy configurations, see [Help secure Windows PCs with Endpoint Protection for Microsoft Intune](../Topic/Help_secure_Windows_PCs_with_Endpoint_Protection_for_Microsoft_Intune.md). <br /> <br />|
|**0x80043001** <br /> <br />|Enrollment package is out of date. <br /> <br />|Download and install the current client software package from the **Admin** workspace. For instructions, see the [Install the Windows PC client with Microsoft Intune](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md) topic. <br /> <br />|
|**0x80043004** <br /> <br />|Subscription does not exist, or is disabled. <br /> <br />|Verify that your account and subscription to [!INC[wit_nextref](../Token/wit_nextref_md.md)] is still active. To view your account settings, sign in to your account in the [Microsoft Intune account portal](http://go.microsoft.com/fwlink/?LinkId=247978). <br /> <br />|
|**0x80043002** <br /> <br />|Account is in maintenance mode. <br /> <br />|You cannot enroll new client computers when the account is in maintenance mode. To view your account settings, sign in to your account in the [Microsoft Intune account portal](http://go.microsoft.com/fwlink/?LinkId=247978). <br /> <br />|
|**0x80043003** <br /> <br />|Account is deleted. <br /> <br />|Verify that your account and subscription to [!INC[wit_nextref](../Token/wit_nextref_md.md)] is still active. To view your account settings, sign in to your account in the [Microsoft Intune account portal](http://go.microsoft.com/fwlink/?LinkId=247978). <br /> <br />|
|**0x80043005** <br /> <br />|The client computer is retired. <br /> <br />|Wait a few hours, remove any older versions of the client software from the computer, and then retry the client software installation. For instructions, see [What to do if the client will not uninstall from the Microsoft Intune administrator console](../Topic/Troubleshoot_Endpoint_Protection_in_Microsoft_Intune.md#BKMK_Whattodo). <br /> <br />|
|**0x80043006** <br /> <br />|The maximum number of seats allowed for the account is reached. <br /> <br />|Your organization must purchase additional seats before you can enroll more client computers in the service. <br /> <br />|
|**0x80043007** <br /> <br />|Could not find the certificate file in the same folder as the installer program. <br /> <br />|Extract all files before you start the installation. Do not rename or relocate any of the extracted files: all files must exist in the same folder or the installation will fail. For more information, see [Install the Windows PC client with Microsoft Intune](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md). <br /> <br />|
|**0x8024D015**, **0x00240005**, **0x80070BC2**, **0x80070BC9**, **0x80CFD015** <br /> <br />|The software cannot be installed because a restart of the client computer is pending. <br /> <br />|Restart the computer and then retry the client software installation. <br /> <br />|
|**0x80070032** <br /> <br />|One or more prerequisites for installing the client software were not found on the client computer. <br /> <br />|Make sure that all required updates are installed on the client computer and then retry the client software installation. For more information about prerequisites for installing the client software, see [Network infrastructure requirements for Microsoft Intune](../Topic/Network_infrastructure_requirements_for_Microsoft_Intune.md). <br /> <br />|
|**0x80043008** <br /> <br />|Could not start the Microsoft Online Management Updates service. <br /> <br />|Contact [Support](http://go.microsoft.com/fwlink/?LinkID=246606). <br /> <br />|
|**0x80043009** <br /> <br />|The client computer is already enrolled into the service. <br /> <br />|You must retire the client computer before you can re-enroll it in the service. For instructions, see [What to do if the client will not uninstall from the Microsoft Intune administrator console](../Topic/Troubleshoot_Endpoint_Protection_in_Microsoft_Intune.md#BKMK_Whattodo). <br /> <br />|
|**0x8004300B** <br /> <br />|The client software installation package cannot run because the version of Windows that is running on the client is not supported. <br /> <br />|[!INC[wit_firstref](../Token/wit_firstref_md.md)] does not support the version of Windows that is running on the client computer. For a list of supported operating systems, see [Network infrastructure requirements for Microsoft Intune](../Topic/Network_infrastructure_requirements_for_Microsoft_Intune.md). <br /> <br />|
|**0xAB2** <br /> <br />|The Windows Installer could not access VBScript run time for a custom action. <br /> <br />|This error is caused by a custom action that is based on Dynamic-Link Libraries (DLLs). When troubleshooting the DLL, you might have to use the tools that are described in [Microsoft Support KB198038: Useful Tools for Package and Deployment Issues](http://go.microsoft.com/fwlink/?LinkID=234255). <br /> <br />|
|**0x8004300f** <br /> <br />|The software cannot be installed because the System Center Configuration Manager client is already installed. <br /> <br />|Remove the Configuration Manager client and then retry the client software installation. <br /> <br />|
|**0x80043010** <br /> <br />|The software cannot be installed because the Open Mobile Alliance Device Management (OMADM) client is already installed. <br /> <br />|Un-enroll the OMADM client and then retry the client software installation. <br /> <br />|
If installation problems persist, contact [Support](http://go.microsoft.com/fwlink/?LinkID=246606). Have the client computer enrollment log (located in %*programfiles*%\Microsoft\OnlineManagement\Logs\Enrollment.log and %*userprofile*%\AppData\Local\Microsoft\OnlineManagement\Logs\Enrollement.log) and Windows Update log (%*windir*%\windowsupdate.log) available to show to support engineers.

