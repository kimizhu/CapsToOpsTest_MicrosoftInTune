---
description: na
keywords: na
pagetitle: Old - Computer capabilities in Intune
search: na
ms.author: f93f38ed286b4cbb94b9b427a0abc63e
ms.date: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7fe70f6c-3d8d-4041-a2cf-04d33af11a68
---
# Old - Computer capabilities in Intune
Devices that run Windows 8.1 and Windows 10 can be managed using the Intune client. You can deploy software to your managed computers in a variety of different formats like a Windows Installer, or Windows app package file. You can also deploy links to applications in a store, or links to Web applications.

## <a name="BKMK_ClientReqs"></a>Supported computers
**Operating Systems**: 
You can install the [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] client on computers that run the following operating systems:

|Operating system <br /> <br />|System architecture <br /> <br />|
|--------------------|-----------------------|
|[!INCLUDE[windowsvista](../Token/windowsvista_md.md)] <br /> <br /><ul><li>Business </li><li>Enterprise </li><li>Ultimate </li> </ul>|x86, x64 <br /> <br />|
|[!INCLUDE[nextref_client_7](../Token/nextref_client_7_md.md)] <br /> <br /><ul><li>Professional (with no service pack, or with SP1) </li><li>Enterprise (with no service pack, or with SP1) </li><li>Ultimate (with no service pack, or with SP1) </li> </ul>|x86, x64 <br /> <br />|
|[!INCLUDE[win8_client_2](../Token/win8_client_2_md.md)] <br /> <br /><ul><li>Pro </li><li>Enterprise </li> </ul>|x86, x64 <br /> <br />|
|[!INCLUDE[winblue_client_2](../Token/winblue_client_2_md.md)] <br /> <br /><ul><li>Pro </li><li>Enterprise </li> </ul>|X86, x64 <br /> <br />|
**Hardware**:
The following are minimum hardware requirements for installing the [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] client:

|Requirement <br /> <br />|More information <br /> <br />|
|---------------|--------------------|
|Network <br /> <br />|The client requires the computer to have Internet connectivity and access to the domains defined in the [Network infrastructure](../Topic/Network_infrastructure_requirements_for_Microsoft_Intune.md#BKMK_NetworkReqs) section of this topic. <br /> <br />|
|Processor and Memory <br /> <br />|Refer to the processor and RAM requirements for the computer's operating system. <br /> <br />|
|Disk space <br /> <br />|200 MB available disk space before the client software is installed. <br /> <br />|
**Software**: 
The following are software requirements for installing the [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] client:

|Requirement <br /> <br />|More information <br /> <br />|
|---------------|--------------------|
|Administrative permissions <br /> <br />|The account that installs the client software must have local administrator permissions to that computer. <br /> <br />|
|Windows Installer 3.1 <br /> <br />|The computer must have, at a minimum, Windows Installer 3.1. <br /> <br />To view the version of Windows Installer on a client computer: <br /> <br /><ul><li>On the computer, right-click **%windir%\System32\msiexec.exe**, and then click **Properties**. </li> </ul>You can download the latest version of Windows Installer from [Windows Installer Redistributables](http://go.microsoft.com/fwlink/?LinkID=234258) on the Microsoft Developer Network website. <br /> <br />|
|Remove incompatible client software <br /> <br />|Before you install the [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] client software, you must uninstall the following client software from that computer: <br /> <br /><ul><li>Any version of [!INCLUDE[cm5short](../Token/cm5short_md.md)] </li><li>Any version of [!INCLUDE[sccmshortname](../Token/sccmshortname_md.md)] </li><li>Any version of Systems Management Server </li> </ul>|

## <a name="WIT_Cap"></a>Computer management features
**Intune computer management capabilities:**

- **Manage software updates.** You can keep computers up-to-date, and manage when updates are applied.

- **Set Windows firewall policy.** This helps to ensure that no computer used by your company has an inactive or improperly-configured firewall.

- **Anti-malware protection.**[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] includes [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Endpoint Protection, and allows you to set policies to ensure that computers are kept up-to-date with the latest anti-malware definition updates.

- **Remote assistance.**[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] allows users to contact IT support staff, who can then provide assistance using a remote desktop feature that is included with [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

- **Software license** management.  Track how many software licenses are available, and how many available licenses are being used.

