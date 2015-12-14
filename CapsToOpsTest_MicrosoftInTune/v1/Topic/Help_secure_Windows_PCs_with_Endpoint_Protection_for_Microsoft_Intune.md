---
description: na
keywords: na
pagetitle: Help secure Windows PCs with Endpoint Protection for Microsoft Intune
search: na
ms.author: f93f38ed286b4cbb94b9b427a0abc63e
ms.date: 2015-08-31
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 682a83ec-bcf4-46ed-9a74-61b87b6a86a3
---
# Help secure Windows PCs with Endpoint Protection for Microsoft Intune
[!INC[wit_firstref](../Token/wit_firstref_md.md)] can help you to secure your managed computers in a number of ways, including Endpoint Protection which provides real-time protection against malware threats, keeps malware definitions up-to date, and automatically scans computers. [!INC[epshort](../Token/epshort_md.md)] also provides tools that help you to manage and monitor malware attacks

If you have not yet installed the [!INC[wit_nextref](../Token/wit_nextref_md.md)] client on your computers, see [Install the Windows PC client with Microsoft Intune](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md).

Use the information in the following sections to help you configure, deploy and monitor [!INC[epshort](../Token/epshort_md.md)].

## Using Endpoint Protection in Microsoft Intune

### Before you start
As an IT admin, one of your top priorities is to keep the computers that you manage free of malware and viruses. Before you deploy [!INC[wit_firstref](../Token/wit_firstref_md.md)] to client computers in your organization, you should decide how to protect your computers by selecting one of the following options and configuring its associated policy settings:

|I want to: <br /> <br />|Endpoint Protection policy settings <br /> <br />|More information <br /> <br />|
|--------------|---------------------------------------|--------------------|
|Use [!INC[wit_firstref](../Token/wit_firstref_md.md)][!INC[epshort](../Token/epshort_md.md)] only if no third-party endpoint protection application is installed <br /> <br />You can use [!INC[wit_firstref](../Token/wit_firstref_md.md)][!INC[epshort](../Token/epshort_md.md)] on all computers where a third-party endpoint protection application is not installed. <br /> <br />|<ul><li>Install Endpoint Protection = **Yes** </li><li>Enable Endpoint Protection = **Yes** </li><li>Install Endpoint Protection even if a third-party endpoint protection application is installed = **No** </li> </ul>|If a third-party endpoint protection application is detected, [!INC[wit_firstref](../Token/wit_firstref_md.md)][!INC[epshort](../Token/epshort_md.md)] will not be installed, or will be uninstalled if it has already been installed. <br /> <br />|
|Use [!INC[wit_firstref](../Token/wit_firstref_md.md)][!INC[epshort](../Token/epshort_md.md)], even if a third-party endpoint protection application is installed <br /> <br />With this approach, you will be running [!INC[wit_firstref](../Token/wit_firstref_md.md)][!INC[epshort](../Token/epshort_md.md)] and the third party endpoint protection application (if it is installed) simultaneously. This is not a recommended configuration because of potential performance issues. <br /> <br />|<ul><li>Install Endpoint Protection = **Yes** </li><li>Enable Endpoint Protection = **Yes** </li><li>Install Endpoint Protection even if a third-party endpoint protection application is installed = **Yes** </li> </ul>|Use when: <br /> <br /><ul><li>You want to switch to using [!INC[wit_firstref](../Token/wit_firstref_md.md)][!INC[epshort](../Token/epshort_md.md)]. </li><li>You deploy a new client that will use [!INC[wit_firstref](../Token/wit_firstref_md.md)][!INC[epshort](../Token/epshort_md.md)] </li><li>You upgrade any client that will use [!INC[wit_firstref](../Token/wit_firstref_md.md)][!INC[epshort](../Token/epshort_md.md)]. </li> </ul>|
|Use [!INC[wit_firstref](../Token/wit_firstref_md.md)] without [!INC[wit_firstref](../Token/wit_firstref_md.md)][!INC[epshort](../Token/epshort_md.md)] <br /> <br />In this case, you won’t be using [!INC[wit_firstref](../Token/wit_firstref_md.md)][!INC[epshort](../Token/epshort_md.md)] to protect your computers from malware and viruses. Instead, you will rely on a third-party endpoint protection application. <br /> <br />|<ul><li>Install Endpoint Protection = **No** </li> </ul>|If you are not using a third-party endpoint protection application, this configuration is not recommended, as it could expose your organization’s computers to malware or other attacks. <br /> <br />[!INC[wit_firstref](../Token/wit_firstref_md.md)][!INC[epshort](../Token/epshort_md.md)] is not installed, and it is uninstalled if it was installed previously. <br /> <br />|
If you want to switch from your current endpoint protection application to [!INC[wit_firstref](../Token/wit_firstref_md.md)][!INC[epshort](../Token/epshort_md.md)], use the following steps which are explained in more detail later in this topic:

1. Leave your current endpoint protection application running while you deploy the [!INC[wit_nextref](../Token/wit_nextref_md.md)] client software to those computers.

2. Confirm that [!INC[wit_firstref](../Token/wit_firstref_md.md)][!INC[epshort](../Token/epshort_md.md)] is installed and is helping to secure client computers.

3. Remove the third-party endpoint protection software by:

   - Using [!INC[wit_nextref](../Token/wit_nextref_md.md)] software distribution to deploy a software removal tool that is provided by the manufacturer of the third-party endpoint protection application. For more information, see [Deploy and configure apps with Microsoft Intune](../Topic/Deploy_and_configure_apps_with_Microsoft_Intune.md).

   - Removing the third-party endpoint protection application manually.

> [!NOTE]
> [!INC[wit_nextref](../Token/wit_nextref_md.md)] will not uninstall third-party endpoint protection applications.

### <a name="BKMK_HowtoConf"></a>How to configure Microsoft Intune Endpoint Protection
Use the following procedure to help you configure [!INC[epshort](../Token/epshort_md.md)] for [!INC[wit_firstref](../Token/wit_firstref_md.md)]. [!INC[wit_nextref](../Token/wit_nextref_md.md)] can manage [!INC[epshort](../Token/epshort_md.md)] for Windows 10 Technical Preview. Certain policy settings are only available for Windows 10.

1. In the [Microsoft Intune administration console](https://manage.microsoft.com/), click **Policy** &gt; **Add Policy**.

2. Configure and deploy a **Microsoft Intune Agent Settings** policy for the [!INC[epshort](../Token/epshort_md.md)] settings. You can use recommended settings or customize the settings. If you need more information about how to create and deploy policies, see the [Common Windows PC management tasks with the Microsoft Intune computer client](../Topic/Common_Windows_PC_management_tasks_with_the_Microsoft_Intune_computer_client.md) topic.

   The tables after this procedure show the values you can configure in the policy and also the recommended values that will be used if you don’t customize the policy. You can find these settings in the **Endpoint Protection** section.

You can view the deployed [!INC[epshort](../Token/epshort_md.md)] policy on the **All Policies** page of the **Policy** workspace.

#### Endpoint Protection service settings

|Policy setting <br /> <br />|More information <br /> <br />|
|------------------|--------------------|
|**Install Endpoint Protection** <br /> <br />|Set to **Yes** to install [!INC[epshort](../Token/epshort_md.md)] on managed computers. If a third-party endpoint protection application is detected during installation, [!INC[epshort](../Token/epshort_md.md)] will not be installed unless **Install Endpoint Protection even if a third party endpoint protection application is installed** is set to **Yes**. **Note:** Intune [!INC[epshort](../Token/epshort_md.md)] is installed on managed computers by default. If you don’t want [!INC[epshort](../Token/epshort_md.md)] installed on your managed computers, you must explicitly set this policy to **No**. If [!INC[epshort](../Token/epshort_md.md)] was previously installed and the policy is updated to **No**, then the [!INC[epshort](../Token/epshort_md.md)] client will be uninstalled. <br />Recommended value: **Yes** <br /> <br />|
|**Install Endpoint Protection even if a third party endpoint protection application is installed** <br /> <br />|Set to **Yes** to install [!INC[wit_firstref](../Token/wit_firstref_md.md)][!INC[epshort](../Token/epshort_md.md)] even if a third-party endpoint protection application is detected. <br /> <br />Recommended value: **Yes** <br /> <br />|
|**Enable Endpoint Protection** <br /> <br />|Set to **Yes** to enable [!INC[wit_firstref](../Token/wit_firstref_md.md)][!INC[epshort](../Token/epshort_md.md)] on computers which have the [!INC[epshort](../Token/epshort_md.md)] client. <br /> <br />If set to **No**, and [!INC[wit_firstref](../Token/wit_firstref_md.md)][!INC[epshort](../Token/epshort_md.md)] is installed, the [!INC[epshort](../Token/epshort_md.md)] client user interface is not displayed to users and all protection features are inactive. <br /> <br />Recommended value: **Yes** <br /> <br />|
|**Disable Client UI** <br /> <br />|Set to **Yes** to hide the [!INC[wit_firstref](../Token/wit_firstref_md.md)][!INC[epshort](../Token/epshort_md.md)] client user interface from users (requires a client computer restart to take effect). <br /> <br />Recommended value: **No** <br /> <br />|
|**Install Endpoint Protection even if a third party endpoint protection application is installed** <br /> <br />|Set to **Yes** to force the installation of [!INC[wit_firstref](../Token/wit_firstref_md.md)][!INC[epshort](../Token/epshort_md.md)], even if a third-party endpoint protection application is detected. <br /> <br />Recommended value: **No** <br /> <br />|
|**Create a system restore point before malware remediation** <br /> <br />|Set to **Yes** to create a Windows System Restore Point before any malware remediation begins. <br /> <br />Recommended value: **Yes** <br /> <br />|
|**Track resolved malware (days)** <br /> <br />|Lets [!INC[epshort](../Token/epshort_md.md)] track resolved malware for a specified time so that you can manually check previously infected computers. <br /> <br />You can specify a value from 0 to 30 days. <br /> <br />Recommended value: **7 days** <br /> <br />|
If you have set the policy values for **Install Endpoint Protection** and **Enable Endpoint Protection** to **Yes**, and the policy value for  **Install Endpoint Protection even if a third party endpoint protection application is installed** to **No**, [!INC[wit_firstref](../Token/wit_firstref_md.md)][!INC[epshort](../Token/epshort_md.md)] will detect that another endpoint protection application is installed and will be not be installed, or uninstalled if it is already present (however, [!INC[wit_firstref](../Token/wit_firstref_md.md)][!INC[epshort](../Token/epshort_md.md)] does report about the health of the other endpoint protection application in the [!INC[wit_adminconsole](../Token/wit_adminconsole_md.md)]).

#### Real-time protection settings

|Policy setting <br /> <br />|More information <br /> <br />|
|------------------|--------------------|
|**Enable real-time protection** <br /> <br />|Enables monitoring and scanning of all files and applications that are accessed. It also blocks any malicious files and applications before they can run on computers. <br /> <br />Recommended value: **Yes** <br /> <br />|
|**Scan all downloads** <br /> <br />|Enables the scanning of all files and attachments that are downloaded from the Internet to computers. <br /> <br />Recommended value: **Yes** <br /> <br />|
|**Monitor file and program activity on computers** <br /> <br />|Enables the monitoring of incoming files and outgoing files, and program activity on computers. With this setting, [!INC[epshort](../Token/epshort_md.md)] can monitor when files and programs start to run and alert you about any actions they perform or actions that are taken on them. <br /> <br />Recommended value: **Yes** <br /> <br />|
|**Files monitored** <br /> <br />|If **Monitor file and program activity on computers** is enabled, this setting allows you to choose if only incoming, only outgoing, or all files are monitored. <br /> <br />Recommended value: **Monitor all files** <br /> <br />|
|**Enable behavior monitoring** <br /> <br />|Allows [!INC[wit_firstref](../Token/wit_firstref_md.md)][!INC[epshort](../Token/epshort_md.md)] to check for certain patterns of suspicious activity on client computers. <br /> <br />Recommended value: **Yes** <br /> <br />|
|**Enable Network Inspection System** <br /> <br />|Enables Network Inspection System (NIS) on client computers. NIS uses signatures of known vulnerabilities from the [Microsoft Malware Protection Center](http://go.microsoft.com/fwlink/?LinkId=234249)  to help detect and block malicious network traffic. <br /> <br />Recommended value: **Yes** <br /> <br />|

#### Scan schedule settings

|Policy setting <br /> <br />|More information <br /> <br />|
|------------------|--------------------|
|**Schedule a daily quick scan** <br /> <br />|Schedules a daily quick scan of both frequently used files and important system files on computers. This quick scan has a minimal effect on performance. <br /> <br />Recommended value: **Yes** <br /> <br />|
|**Run a quick scan if you have missed two consecutive scans** <br /> <br />|Configures [!INC[epshort](../Token/epshort_md.md)] to automatically run a quick scan on computers if they miss two consecutive, scheduled quick scans. <br /> <br />Recommended value: **Yes** <br /> <br />|
|**Schedule a full scan** <br /> <br />|Configures a full scan of all files and resources on the local hard disks of computers. This scan can take some time and can affect computer performance (depending on the number of files and resources scanned). <br /> <br />Recommended value: **No** <br /> <br />|
|**Run a full scan if you have missed two consecutive full scans** <br /> <br />|Configures [!INC[epshort](../Token/epshort_md.md)] to automatically run a full scan on computers if they miss two consecutive, scheduled full scans. <br /> <br />Recommend value: Not configured <br /> <br />|

#### Scan options settings

|Policy setting <br /> <br />|More information <br /> <br />|
|------------------|--------------------|
|**Run a full scan after installation of Endpoint Protection** <br /> <br />|Configures [!INC[epshort](../Token/epshort_md.md)] to automatically run a full system scan after it is installed on computers. This scan runs only when computers are idle to minimize the effect on user productivity. <br /> <br />Recommended value: **Yes** <br /> <br />|
|**Automatically run a full scan when needed to follow up malware removal** <br /> <br />|Set to **Yes** to let [!INC[epshort](../Token/epshort_md.md)] automatically run a full system scan on computers after the removal of malware to help confirm that other files were not affected. <br /> <br />Recommended value: **Yes** <br /> <br />|
|**Start a scheduled scan only when the computer is idle** <br /> <br />|Set to **Yes** to prevent scheduled scans from starting when computers are in use to prevent any loss of user productivity. <br /> <br />Recommended value: **Yes** <br /> <br />|
|**Check for the latest malware definitions before starting a scan** <br /> <br />|Set to **Yes** to let [!INC[epshort](../Token/epshort_md.md)] automatically check for the latest malware definitions before it starts a scan on computers. <br /> <br />Recommended value: **Yes** <br /> <br />|
|**Scan archive files** <br /> <br />|Set to **Yes** to configure [!INC[epshort](../Token/epshort_md.md)] to scan for malware in archive files (like .zip or .cab files) on computers. <br /> <br />Recommended value: **No** <br /> <br />|
|**Scan email messages** <br /> <br />|Set to **Yes** to configure [!INC[epshort](../Token/epshort_md.md)] to scan incoming email messages when they arrive on computers. <br /> <br />Recommended value: **Yes** <br /> <br />|
|**Scan files opened from network shared folders** <br /> <br />|Set to **Yes** to configure [!INC[epshort](../Token/epshort_md.md)] to scan files that are opened from shared folders on the network. These are typically files that are accessed by using a UNC path. Enabling this feature can cause problems for users who have read-only access because they cannot remove malware. <br /> <br />Recommended value: **No** <br /> <br />|
|**Scan mapped network drives** <br /> <br />|Set to **Yes** to configure [!INC[epshort](../Token/epshort_md.md)] to scan files on mapped network drives. Enabling this feature can cause problems for users who have read-only access because they cannot remove malware. <br /> <br />Recommended value: **No** <br /> <br />|
|**Scan removable drives** <br /> <br />|Set to **Yes** to configure [!INC[epshort](../Token/epshort_md.md)] to scan for malware and unwanted software in the contents of removable drives, like USB flash drives, when you run a full scan on computers. <br /> <br />Recommended value: **Yes** <br /> <br />|
|**Limit CPU usage during a scan** <br /> <br />|Configures the maximum percentage of CPU usage that can be used during scheduled scans on computers. You can set this value from 1 to 100 percent. <br /> <br />Recommended value: **50%** <br /> <br />|

#### Default actions settings

|Policy setting <br /> <br />|More information <br /> <br />|
|------------------|--------------------|
|**Choose how Endpoint Protection acts on malware of the following alert levels** <br /> <br />|Specifies the default action that [!INC[epshort](../Token/epshort_md.md)] takes when malware of various alert levels is detected. <br /> <br />For each alert level, you can remove the malware, quarantine it, or take Microsoft’s recommended action. <br /> <br />Recommended value: **Recommended action** <br /> <br />|

#### Excluded files and folders settings

|Policy setting <br /> <br />|More information <br /> <br />|
|------------------|--------------------|
|**Files and folders to exclude when running a scan or using real-time protection** <br /> <br />|Excludes specific files or folders when a scan is run or when real-time protection is used on computers. <br /> <br />|

#### Excluded processes settings

|Policy setting <br /> <br />|More information <br /> <br />|
|------------------|--------------------|
|**Processes to exclude when running a scan or using real-time protection** <br /> <br />|Lets you exclude specific processes when a scan is run or from real-time protection. You can exclude only files with the following extensions: **.exe**, **.com** or **.scr**. <br /> <br />|

#### Excluded file types settings

|Policy setting <br /> <br />|More information <br /> <br />|
|------------------|--------------------|
|**File extensions to exclude when running a scan or using real-time protection** <br /> <br />|Lets you exclude specific file name extensions when a scan is run or when real-time protection is used on computers. <br /> <br />|

#### Microsoft Active Protection Service Settings
Microsoft Active Protection Service is an online community that helps you decide how to respond to potential threats. The community also helps stop the spread of new malware infections.

|Policy setting <br /> <br />|More information <br /> <br />|
|------------------|--------------------|
|**Join Microsoft Active Protection Service** <br /> <br />|**Yes** automatically sends information about detected malware to the Microsoft Active Protection Service. Microsoft does not use any information collected to identify you or to contact you. <br /> <br />Recommended value: **Yes** <br /> <br />|
|**Membership level** <br /> <br />|If you selected to join the Microsoft Active Protection Service, this setting lets you choose from one of the following membership levels: <br /> <br /><ul><li>**Basic** - Sends basic information to Microsoft about detected malware. This includes where the software came from, the actions that you apply or that [!INC[epshort](../Token/epshort_md.md)] applies automatically, and whether the actions were successful. </li><li>**Advanced** - Sends more information to Microsoft about malware, spyware, and potentially unwanted software. This includes the location of the software, file names, how the software operates, and how it has affected your computer. </li> </ul>Recommended value: **Advanced** <br /> <br />|
|**Receive dynamic definitions based on Microsoft Active Protection Service reports** <br /> <br />|**Yes** lets computers receive dynamic malware definitions based on information that [!INC[epshort](../Token/epshort_md.md)] sends to the Microsoft Active Protection Service (if you have joined it) about detected malware. <br /> <br />Recommended value: **Yes** <br /> <br />|

### Management tasks for Endpoint Protection
The following tasks help you to carry out various management tasks on managed computers that run [!INC[epshort](../Token/epshort_md.md)].

|I want to <br /> <br />|From the [!INC[wit_firstref](../Token/wit_firstref_md.md)] console <br /> <br />|From the managed computer <br /> <br />|
|-------------|--------------------------------------------------------------------------|-----------------------------|
|Update malware definitions <br /> <br />|From the **Groups** workspace, select the computers you want to update. <br /> <br />Click **Remote Tasks** &gt; **Update Malware Definitions**. <br /> <br />|Start the [!INC[epshort](../Token/epshort_md.md)] client software from the Windows notification area. <br /> <br />Click the **Update** tab, and then click **Update**. <br /> <br />|
|Run a malware scan <br /> <br />|From the **Groups** workspace, select the computers you want to scan. <br /> <br />Click **Run a Full Malware Scan** or **Run a Quick Malware Scan**. <br /> <br />|Start the [!INC[epshort](../Token/epshort_md.md)] client software from the Windows notification area. <br /> <br />Select **Quick**, **Full**, or **Custom**, and then click **Scan now**. <br /> <br />|
You can view the status of a remote task by clicking the **Remote Tasks** link in the bottom right corner of the [!INC[wit_adminconsole](../Token/wit_adminconsole_md.md)].

The **Remote Task Status** dialog box lists current remote tasks, task status, device name, any reported errors, and provides a link to troubleshooting information, if appropriate.

### <a name="BKMK_SCEPmon"></a>How to monitor Endpoint Protection
You monitor the status of malware on your computers by using the **Protection** workspace of the [Microsoft Intune administration console](https://manage.microsoft.com/). This workspace contains two pages:

|Page name <br /> <br />|More information <br /> <br />|
|-------------|--------------------|
|**Endpoint Protection Overview** <br /> <br />|Displays important issues as links that you can click for more information. Issues that might be displayed include: <br /> <br /><ul><li>**Malware instances that need follow-up** – Click the link to see a list of malware issues including the follow up action that needs to be taken to resolve the issue. You can further drill into this list to see which computers are affected. </li><li>**Computers with malware that need follow-up** – Click the link to see all computers with unresolved malware issues including the follow up action that needs to be taken to resolve the issue. </li><li>**Devices that are not protected** – Click the link to see computers that are not protected by any endpoint protection software, either because no software is installed, or because there is an error. Select a computer to view more details. </li><li>**Devices with another endpoint protection application running** – Click the link to see computers that are running a third-party endpoint protection application. </li> </ul>|
|**All Malware** <br /> <br />|Displays a list of all active malware found on your computers. You can drill into this list to see all computers that are affected by a particular piece of malware, or you can select one of the following tasks: <br /> <br /><ul><li>**View Properties** – Opens a page with more information about the selected malware. </li><li>**Learn About This Malware** – Opens a topic from the Microsoft Malware Protection Center with more information about the malware. </li> </ul>|
> [!IMPORTANT]
> The **Protection** workspace is not displayed in the administrator console until you have installed the client on, and are successfully managing at least one computer client.

### How to view Recent Detection Paths for malware on computers
Intune can display the paths of up to 10 most recently detected instances of malware on a device. The **Recent Detection Path** is disabled by default. To enable this view:

##### How to enable Recent Detection Paths for malware

1. In the [Microsoft Intune administration console](https://manage.microsoft.com/) go **Groups** &gt; **All Devices** . **Malware**.

2. Right-click a column header. A list of available columns appears.

3. Mark the **Recent Detection Paths** checkbox in the list. The **Recent Detection Paths** column appears and displays up to 10 most recent malware instances monitored on the device.

## Need more help?
For further help and support, see [Troubleshoot Endpoint Protection in Microsoft Intune](../Topic/Troubleshoot_Endpoint_Protection_in_Microsoft_Intune.md).

## See Also
[Manage Windows PCs with Microsoft Intune](../Topic/Manage_Windows_PCs_with_Microsoft_Intune.md)

