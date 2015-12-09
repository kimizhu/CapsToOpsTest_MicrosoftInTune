---
description: na
search: na
title: Update%20apps%20using%20Microsoft%20Intune
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.date: 2015-11-17
ms.author: dbdc710f437843008017318979c6adba
---
# Update%20apps%20using%20Microsoft%20Intune
[!INC[wit_firstref](../Token/wit_firstref_md.md)] can help you manage app updates. Use the information in this topic to understand how you can update apps when a new version is required.

## How to update apps
When a new version of an app you have deployed is released, [!INC[wit_nextref](../Token/wit_nextref_md.md)] lets you update and deploy the newer version of the app. You can only replace a deployment with a newer version of the same app (using the same identifier). You cannot use app updates to update a deployment with a different app package.

> [!IMPORTANT]
> When you deploy an app with a deployment action of **Required install** and later change the deployment action to **Available install**, updates to the app are not automatically installed on devices that installed the app before the deployment change was made. To fix this issue, you can do the following:
> 
> - Have the user of the device go to the company portal, select the installed app, and have them click **Install**.
> - Change the deployment action to **Uninstall**, and after the app has been uninstalled, redeploy the app with a deployment action of **Available install**.

#### To update an app

1. In the [Microsoft Intune administrator console](https://account.manage.microsoft.com/admin/default.aspx), click **Apps** &gt; **Apps**.

2. From the **Apps** list, select the app you want to update, and then click **Edit**.

3. In the **Edit Software** wizard, supply any new details for the app package.

4. When you are finished, click **Update**.

When devices next check for available apps, the app will be automatically updated to the latest version.

## See Also
[Deploy and configure apps with Microsoft Intune](../Topic/Deploy_and_configure_apps_with_Microsoft_Intune.md)
[Retire apps using Microsoft Intune](../Topic/Retire_apps_using_Microsoft_Intune.md)

