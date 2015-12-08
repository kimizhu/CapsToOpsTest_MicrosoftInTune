---
description: na
search: na
title: Windows PC management capabilities in Microsoft Intune
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.date: 2015-11-17
ms.author: dbdc710f437843008017318979c6adba
---
# Windows PC management capabilities in Microsoft Intune
You can use [!INC[wit_nextref](../Token/wit_nextref_md.md)] to manage Windows PCs with the Intune client installed. PC management lets you deploy apps and software including software updates to your managed PCs, manage Endpoint Protection and the Windows Firewall, and more.  Below are a list of supported configurations and capabilities.

## <a name="BKMK_ClientReqs"></a>Requirements for PC management
**Operating Systems**: 
You can install the [!INC[wit_nextref](../Token/wit_nextref_md.md)] client on PCs that run the following operating systems (both x86 and x64):

- **Windows Vista** - Business, Enterprise and Ultimate versions.

- **Windows 7** - Professional, Enterprise, and Ultimate versions (with no service pack, or with SP1).

- **Windows 8** - Professional and Enterprise versions.

- **Windows 8.1** - Professional and Enterprise versions.

- **Windows 10** - Professional and Enterprise versions.

**Hardware**:
The following are minimum hardware requirements for installing the [!INC[wit_nextref](../Token/wit_nextref_md.md)] client:

|Requirement <br /> <br />|More information <br /> <br />|
|---------------|--------------------|
|Network <br /> <br />|The client requires the PC to have Internet connectivity. <br /> <br />|
|Processor and Memory <br /> <br />|Refer to the processor and RAM requirements for the PC's operating system. <br /> <br />|
|Disk space <br /> <br />|200 MB available disk space before the client software is installed. <br /> <br />|
**Software**: 
The following are software requirements for installing the [!INC[wit_nextref](../Token/wit_nextref_md.md)] client:

|Requirement <br /> <br />|More information <br /> <br />|
|---------------|--------------------|
|Administrative permissions <br /> <br />|The account that installs the client software must have local administrator permissions to that PC. <br /> <br />|
|Windows Installer 3.1 <br /> <br />|The PC must have, at a minimum, Windows Installer 3.1. <br /> <br />To view the version of Windows Installer on a PC: <br /> <br /><ul><li>On the PC, right-click **%windir%\System32\msiexec.exe**, and then click **Properties**. </li> </ul>You can download the latest version of Windows Installer from [Windows Installer Redistributables](http://go.microsoft.com/fwlink/?LinkID=234258) on the Microsoft Developer Network website. <br /> <br />|
|Remove incompatible client software <br /> <br />|Before you install the [!INC[wit_nextref](../Token/wit_nextref_md.md)] client software, you must uninstall the following client software from that PC: <br /> <br /><ul><li>Any version of [!INC[cm5short](../Token/cm5short_md.md)] </li><li>Any version of [!INC[sccmshortname](../Token/sccmshortname_md.md)] </li><li>Any version of Systems Management Server (SMS) </li> </ul>|

## <a name="WIT_Cap"></a>Intune PC management capabilities

- **Manage software updates** You can keep PCs up-to-date, and manage when updates are applied.

- **Windows Firewall policy** This helps to ensure that no PC used by your company has an inactive or improperly-configured Windows Firewall.

- **Anti-malware protection**[!INC[wit_nextref](../Token/wit_nextref_md.md)] includes Endpoint Protection, which helps protect your PCs from malware.

- **Remote assistance**[!INC[wit_nextref](../Token/wit_nextref_md.md)] allows users to contact IT support staff, who can then provide assistance using a remote desktop feature that is included with [!INC[wit_nextref](../Token/wit_nextref_md.md)].

- **Software license** management.  Track how many software licenses are available, and how many available licenses are being used.

## See Also
[Introduction to Microsoft Intune](../Topic/Introduction_to_Microsoft_Intune.md)
[Manage Windows PCs with Microsoft Intune](../Topic/Manage_Windows_PCs_with_Microsoft_Intune.md)

