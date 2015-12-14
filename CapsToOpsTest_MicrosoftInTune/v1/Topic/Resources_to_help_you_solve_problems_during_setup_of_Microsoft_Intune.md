---
description: na
keywords: na
pagetitle: Resources to help you solve problems during setup of Microsoft Intune
search: na
ms.author: 03258b9b-2cea-4654-ab05-a27214174f4b
ms.date: 5/18/2015 8:00:00 AM
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6865f1fb-c2c1-47af-83f5-5704e7210a49
robots: noindex,nofollow
---
# Resources to help you solve problems during setup of Microsoft Intune
Because [!INC[wit_firstref](../Token/wit_firstref_md.md)] is a cloud service, there should be little need to repair or troubleshoot operational issues. When you experience problems in accessing the service, the following sections can help you identify next steps to take.

## <a name="BKMK_ResolveSetupProblems"></a>Tips to solving problems with setup and configuration of Microsoft Intune
[!INC[wit_nextref](../Token/wit_nextref_md.md)] does not generate setup or operation logs that you can use to troubleshoot problems.

Your administrative actions use a web browser to connect to the cloud service. Problems in accessing the service are typically due to one of the following:

|Problem <br /> <br />|Details <br /> <br />|
|-----------|-----------|
|Insufficient permissions to the [!INC[wit_icp_1](../Token/wit_icp_1_md.md)] <br /> <br />|To use the [!INC[wit_icp_1](../Token/wit_icp_1_md.md)] to manage more than your own user profile, your account must: <br /> <br /><ul><li>have a license to use [!INC[wit_nextref](../Token/wit_nextref_md.md)] </li><li>have a sign-in status of **Allowed** to sign in </li><li>be a [!INC[wit_icp_1](../Token/wit_icp_1_md.md)] tenant administrator </li> </ul>For information, see [Intune administrator accounts and special permissions](../Topic/What_to_know_before_setting_up_Microsoft_Intune.md#BKMK_AdminAccounts). <br /> <br />|
|Network access including: <br /> <br /><ul><li>Domains used by [!INC[wit_nextref](../Token/wit_nextref_md.md)] </li><li>Traffic on the network </li><li>Web browser support </li> </ul>|To connect to [!INC[wit_nextref](../Token/wit_nextref_md.md)], you must: <br /> <br /><ul><li>use a supported web browser </li><li>have access on your network through firewalls and proxy servers to the various domains that are in use by the [!INC[wit_nextref](../Token/wit_nextref_md.md)] service. </li> </ul>For information about requirements and configurations necessary to use [!INC[wit_nextref](../Token/wit_nextref_md.md)], see: <br /> <br /><ul><li>[Infrastructure requirements](../Topic/Network_infrastructure_requirements_for_Microsoft_Intune.md#BKMK_InfrastructureReqs) </li><li>[Web browsers supported by Microsoft Intune](../Topic/Network_infrastructure_requirements_for_Microsoft_Intune.md#BKMK_SupportedBrowsers) </li> </ul>|
|[!INC[wit_nextref](../Token/wit_nextref_md.md)] service availability <br /> <br />|To view details online, or subscribe to RSS feeds about the health of the [!INC[wit_nextref](../Token/wit_nextref_md.md)] service, see: <br /> <br /><ul><li>[Microsoft Intune service](http://status.manage.microsoft.com/) </li> </ul>|

## See Also
[Introduction to Microsoft Intune](../Topic/Introduction_to_Microsoft_Intune.md)

