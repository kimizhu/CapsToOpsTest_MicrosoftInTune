---
description: na
search: na
title: Help protect Windows PCs using Windows Firewall policies in Microsoft Intune
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.date: 2015-08-31
ms.author: eb854939b4ae448eb6d114a05061973b
---
# Help protect Windows PCs using Windows Firewall policies in Microsoft Intune
[!INC[wit_firstref](../Token/wit_firstref_md.md)] can help you to secure your managed computers in a number of ways, including the use of policies that allow you to configure Windows Firewall settings on client computers.

If you have not yet installed the [!INC[wit_nextref](../Token/wit_nextref_md.md)] client on your computers, see [Install the Windows PC client with Microsoft Intune](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md).

Use the information in the following sections to help you configure, deploy and monitor Windows Firewall Policies on client computers.

## <a name="BKMK_Firewall"></a>Using Microsoft Intune policies to manage the Windows Firewall
The Windows Firewall policy lets you create and deploy settings that control the Windows Firewall on managed computers. You cannot manage custom exceptions for Windows Firewall and these settings do not affect third-party firewalls.

> [!NOTE]
> If [!INC[wit_firstref](../Token/wit_firstref_md.md)] policy and Group Policy are configured to manage the same setting on the computer, the Group Policy setting overrides the [!INC[wit_firstref](../Token/wit_firstref_md.md)] policy. For information about how to avoid conflicts between [!INC[wit_firstref](../Token/wit_firstref_md.md)] policies and Group Policy, see [Resolve GPO and Microsoft Intune policy conflicts](../Topic/Resolve_GPO_and_Microsoft_Intune_policy_conflicts.md).
> 
> If you want to deploy Windows Firewall settings to computers running Windows Vista, you must first install [Hotfix KB971800](http://support2.microsoft.com/kb/971800) on these computers.

> [!IMPORTANT]
> To manage the Windows Firewall using [!INC[wit_nextref](../Token/wit_nextref_md.md)], you must ensure that the following two services are enabled on the computers you will manage:
> 
> - Windows Firewall
> - IPsec Policy Agent

#### To configure a Windows Firewall policy

1. In the [Microsoft Intune administration console](https://manage.microsoft.com/), click **Policy** &gt; **Add Policy**.

2. Configure and deploy a **Windows Firewall Settings** policy. You can use recommended settings or customize the settings. If you need more information about how to create and deploy policies, see the [Common Windows PC management tasks with the Microsoft Intune computer client](../Topic/Common_Windows_PC_management_tasks_with_the_Microsoft_Intune_computer_client.md) topic.

   The tables after this procedure show the values you can configure in the policy and also the recommended values that will be used if you don’t customize the policy.

You can view the deployed Windows Firewall policy on the **All Policies** page of the **Policy** workspace.

### Policy settings for Windows Firewall

#### Turn on Windows Firewall

|Policy setting <br /> <br />|More information <br /> <br />|
|------------------|--------------------|
|**Domain profile** <br /> <br />|Enables the Windows Firewall on managed computers while they are connected to domain networks, for example while at the workplace. <br /> <br />Recommended value: **Yes** <br /> <br />|
|**Private profile** <br /> <br />|Enables the Windows Firewall on managed computers while they are connected to trusted networks, for example while on a home network. <br /> <br />Recommended value: **Yes** <br /> <br />|
|**Public profile** <br /> <br />|Enables the Windows Firewall on managed computers while they are connected to untrusted networks in public places, for example while at a coffee shop. <br /> <br />Recommended value: **Yes** <br /> <br />Required operating system: [!INC[firstref_vista](../Token/firstref_vista_md.md)] or later versions <br /> <br />|

#### Block all incoming connections, including those in the list of allowed programs
> [!IMPORTANT]
> If your environment includes managed computers that are running Windows Vista with no service packs installed, you must either install the update associated with [article 971800](http://go.microsoft.com/fwlink/?LinkId=188405) in the Microsoft Knowledge Base or else disable the **Block all incoming connections** policy settings in policies deployed to those computers.

|Policy setting <br /> <br />|More information <br /> <br />|
|------------------|--------------------|
|**Domain profile** <br /> <br />|Blocks all incoming connections while the computers are connected to domain networks, such as at a workplace. This includes those connections in the list of exceptions. <br /> <br />Recommended value: **No** <br /> <br />|
|**Private profile** <br /> <br />|Blocks all incoming connections while the computers are connected to trusted networks, such as a home network. This includes those connections in the list of exceptions. <br /> <br />Recommended value: **No** <br /> <br />|
|**Public profile** <br /> <br />|Blocks all incoming connections while the computers are connected to untrusted networks at public places, such as at a coffee shop. This includes those connections in the list of exceptions. <br /> <br />Recommended value: **No** <br /> <br />Required operating system: [!INC[nextref_vista](../Token/nextref_vista_md.md)] or later versions <br /> <br />|

#### Notify the user when Windows Firewall blocks a new program

|Policy setting <br /> <br />|More information <br /> <br />|
|------------------|--------------------|
|**Domain profile** <br /> <br />|Notifies users when Windows Firewall blocks a new program while the computers are connected to domain networks, such as at a workplace. <br /> <br />Recommended value: **Yes** <br /> <br />|
|**Private profile** <br /> <br />|Notifies users when Windows Firewall blocks a new program while the computers are connected to trusted networks, such as a home network. <br /> <br />Recommended value: **Yes** <br /> <br />|
|**Public profile** <br /> <br />|Notifies users when Windows Firewall blocks a new program while the computers are connected to untrusted networks at public places, such as a coffee shop. <br /> <br />Recommended value: **Yes** <br /> <br />Required operating system: [!INC[nextref_vista](../Token/nextref_vista_md.md)] or later versions <br /> <br />|

#### Predefined Exceptions

|Policy setting <br /> <br />|More information <br /> <br />|
|------------------|--------------------|
|**BranchCache - Content Retrieval** <br /> <br />|If enabled, lets BranchCache clients use HTTP to retrieve content from one another in the distributed mode and from the hosted cache in hosted cache mode. This setting uses HTTP. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[firstref_client_7](../Token/firstref_client_7_md.md)] or later). <br /> <br />|
|**BranchCache - Hosted Cache Client** <br /> <br />|If enabled, lets BranchCache clients use a hosted cache. This setting uses HTTPS. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_client_7](../Token/nextref_client_7_md.md)] or later). <br /> <br />|
|**BranchCache - Hosted Cache Server** <br /> <br />|If enabled, lets BranchCache clients can use a hosted cache to communicate with other clients. This setting uses HTTPS. <br /> <br />Recommend value: Not configured <br /> <br />([!INC[nextref_client_7](../Token/nextref_client_7_md.md)] or later). <br /> <br />|
|**BranchCache - Peer Discovery** <br /> <br />|If enabled, lets BranchCache clients use the WS Discovery protocol to look up content availability on the local subnet. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_client_7](../Token/nextref_client_7_md.md)] or later). <br /> <br />|
|**BITS Peercaching** <br /> <br />|If enabled, lets clients use Background Intelligent Transfer Service (BITS) to find and share files that are stored in the BITS cache on clients in the same subnet. This setting uses WSDAPI and RPC. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**Connect to a Network Projector** <br /> <br />|If enabled, lets users connect to projectors over wired or wireless networks to project presentations. This setting uses WSDAPI. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**Core Networking** <br /> <br />|If enabled, lets clients use IPv4 and IPv6 to connect to network resources. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**Distributed Transaction Coordinator** <br /> <br />|If enabled, allows managed computers to coordinate transactions that update transaction-protected resources, like databases, message queues, and file systems. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**File and Printer Sharing** <br /> <br />|If enabled, allows users to share local files and printers with other users on the network. This setting uses NetBIOS, LLMNR, SMB, and RPC. <br /> <br />Recommended value: Not configured <br /> <br />(Windows XP or later). <br /> <br />|
|**HomeGroup** <br /> <br />|If enabled, allow managed computers to participate in a HomeGroup network. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_client_7](../Token/nextref_client_7_md.md)] or later). <br /> <br />|
|**iSCSI Service** <br /> <br />|If enabled, allows managed computers to connect to iSCSI servers and devices. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**Key Management Service** <br /> <br />|If enabled, lets computers be counted for license compliance in enterprise environments. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**Media Center Extenders** <br /> <br />|If enabled, allows Media Center Extenders to communicate with computers that are running Windows Media Center. This setting uses SSDP and qWave. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**Netlogon Service** <br /> <br />|If enabled, configures a security channel between domain clients and a domain controller for authenticating users and services. This setting uses RPC. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**Network Discovery** <br /> <br />|If enabled, lets computers discover other devices and be discovered by other devices on the network. This setting uses Function Discovery Host and Publication Services and SSDP, NetBIOS, LLMNR, and UPnP network protocols. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**Performance Logs and Alerts** <br /> <br />|If enabled, allows the Performance Logs and Alerts service to be remotely managed. This setting uses RPC. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**Remote Administration** <br /> <br />|If enabled, allows remote administration of the computer. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**Remote Assistance** <br /> <br />|If enabled, lets users of managed computers request remote assistance from other users on the network. This setting uses SSDP, PNRP, Teredo, and UPnP network protocols. <br /> <br />Recommended value: Not configured <br /> <br />(Windows XP or later). <br /> <br />|
|**Remote Desktop** <br /> <br />|If enabled, lets the computer use Remote Desktop to access other computers. <br /> <br />Recommended value: Not configured <br /> <br />(Windows XP or later). <br /> <br />|
|**Remote Event Log Management** <br /> <br />|If enabled, let’s client event logs be viewed and managed remotely. This setting uses Named Pipes and RPC. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**Remote Scheduled Tasks Management** <br /> <br />|If enabled, allows remote management of the task scheduling service. This setting uses RPC. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**Remote Service Management** <br /> <br />|If enabled, allows remote management of local services on clients. This setting uses Named Pipes and RPC. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**Remote Volume Management** <br /> <br />|If enabled, allows remote software and hardware disk volume management. This setting uses RPC. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**Routing and Remote Access** <br /> <br />|If enabled, allows incoming VPN and remote access connections to computers. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**Secure Socket Tunneling Protocol** <br /> <br />|If enabled, allows incoming VPN connections to managed computers by using Secure Socket Tunneling Protocol (SSTP). This setting uses HTTPS. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**SNMP Trap** <br /> <br />|If enabled, lets managed computers receive SNMP Trap service traffic. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**UPnP Framework** <br /> <br />|If enabled, configures the UPnP Framework service on computers to let them discover and use UPnP certified devices. <br /> <br />Recommended value: Not configured <br /> <br />(Windows XP or later). <br /> <br />|
|**Windows Collaboration Computer Name Registration Service** <br /> <br />|If enabled, lets computers find and communicate with other computers by using the Peer Name Resolution Protocol. This setting uses SSDP and PNRP. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**Windows Media Player** <br /> <br />|If enabled, lets users receive streaming media over UDP. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**Windows Media Player Network Sharing Service** <br /> <br />|If enabled, lets users share media over a network. This setting uses the SSDP, qWave, and UPnP network protocols. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**Windows Media Player Network Sharing Service (Internet)** <br /> <br />|If enabled, lets users share home media over the Internet. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_client_7](../Token/nextref_client_7_md.md)] or later). <br /> <br />|
|**Windows Meeting Space** <br /> <br />|If enabled, lets users collaborate over a network to share documents, programs, or their desktop. This setting uses DFSR and P2P. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**Windows Peer to Peer Collaboration Foundation** <br /> <br />|If enabled, configures various peer-to-peer programs and technologies to allow them to connect. This setting uses SSDP and PNRP. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**Windows Remote Management (Compatibility)** <br /> <br />|If enabled, allows remote management of managed computers by using WS-Management, a Web services-based protocol for remote management of operating systems and devices. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|
|**Windows Remote Management** <br /> <br />|If enabled, allows remote management of managed computers by using WS-Management, a Web services-based protocol for remote management of operating systems and devices. <br /> <br />Recommended value: Not configured <br /> <br />(Windows 8 or later) <br /> <br />|
|**Windows Virtual PC** <br /> <br />|If enabled, lets virtual machines, communicate with other computers. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_client_7](../Token/nextref_client_7_md.md)] only) <br /> <br />|
|**Wireless Portable Devices** <br /> <br />|If enabled, allows the transfer of media from a network-enabled camera or media device to managed computers by using the Media Transfer Protocol (MTP). This setting uses SSDP and UPnP network protocols. <br /> <br />Recommended value: Not configured <br /> <br />([!INC[nextref_vista](../Token/nextref_vista_md.md)] or later). <br /> <br />|

## See Also
[Manage Windows PCs with Microsoft Intune](../Topic/Manage_Windows_PCs_with_Microsoft_Intune.md)

