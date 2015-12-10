---
description: na
search: na
title: Reference for Tenant Administrator accounts for Microsoft Intune
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.date: 2015-08-01
ms.author: 2acc2e0c-a3ea-42a3-8a95-f1f50c2bbe2f
capscontentguid: e4eff7b9-4dcd-4959-b1d6-97dc4640dbe2
---
# Reference for Tenant Administrator accounts for Microsoft Intune
Each tenant administrator is assigned one of the following roles:

|Role <br /> <br />|Details <br /> <br />|
|--------|-----------|
|**Billing administrator** <br /> <br />|Makes purchases, manages subscriptions, manages support tickets, and monitors service health. <br /> <br />|
|**Global administrator** <br /> <br />|Has access to all administrative features. By default, the person who signs up to purchase a Microsoft cloud service on behalf of your organization automatically becomes the first global administrator in your tenant. <br /> <br /><ul><li>Only global administrators can assign other administrator roles. </li><li>There can be more than one global administrator at your organization. </li> </ul>|
|**Password administrator** <br /> <br />|Resets passwords, manages service requests, and monitors service health. Password administrators can reset passwords only for users and other password administrators. <br /> <br />|
|**Service support administrator** <br /> <br />|Manages service requests and monitors service health. <br /> <br />|
|**User management administrator** <br /> <br />|Resets passwords, monitors service health, and manages user accounts, user groups, and service requests. <br /> <br />|
Each administrator role has the following associated permissions:

|Permission <br /> <br />|Billing administrator <br /> <br />|Global administrator <br /> <br />|Password administrator <br /> <br />|Service support administrator <br /> <br />|User management administrator <br /> <br />|
|--------------|-------------------------|------------------------|--------------------------|---------------------------------|---------------------------------|
|View organization and user information <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|Manage support tickets <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|
|Reset user passwords <br /> <br />|No <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|No <br /> <br />|Yes; with limitations. This admin cannot reset passwords for billing, global, and service administrators. <br /> <br />|
|Perform billing and purchasing operations <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />|
|Create and manage user views <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|No <br /> <br />|Yes <br /> <br />|
|Create, edit, and delete users and groups, and manage user licenses <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|No <br /> <br />|Yes; with limitations. This admin cannot delete a global administrator or create other administrators. <br /> <br />|
|Manage domains <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />|
|Manage organization information <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />|
|Delegate administrative roles to others <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />|
|Use directory synchronization <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />|
To learn more about administrative accounts in [!INC[wit_firstref](../Token/wit_firstref_md.md)], read about the [different administrative accounts and permissions for separate tasks](http://technet.microsoft.com/library/dn646966.aspx). For help managing administrative users, see [Task 5: Assign administrative users](../Topic/Get_started_with_a_paid_subscription_to_Microsoft_Intune.md#BKMK_AssignAdmins) in [Get started with a paid subscription to Microsoft Intune](../Topic/Get_started_with_a_paid_subscription_to_Microsoft_Intune.md).

