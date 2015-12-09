---
description: na
search: na
title: Manage Internet access using managed browser policies with Microsoft Intune
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.date: 2015-11-23
ms.author: dbdc710f437843008017318979c6adba
---
# Manage Internet access using managed browser policies with Microsoft Intune
The managed browser is a web browsing application that you can deploy in your organization using [!INC[wit_firstref](../Token/wit_firstref_md.md)]. A managed browser policy configures an allow list or a block list that restricts the web sites that users of the managed browser can visit.

Because this app is a managed app, you can also apply mobile application management policies to the app, such as controlling the use of cut, copy and paste, preventing screen captures, and also ensuring that links to content that users click only open in other managed apps. For details, see [Configure and deploy mobile application management policies in the Microsoft Intune console](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md).

> [!IMPORTANT]
> If users install the managed browser themselves on an iOS device with a version less than iOS 9, it will not be managed by any policies you create. To ensure that the browser is managed by [!INC[wit_nextref](../Token/wit_nextref_md.md)], they must uninstall the app before you can deploy it to them as a managed app. On iOS 9 and later, if the user installs the managed browser themselves they will be prompted to allow it to become managed by policy.

You can create managed browser policies for the following device types:

- Devices that run Android 4 and later

- Devices that run iOS 7.1 and later

The [!INC[wit_nextref](../Token/wit_nextref_md.md)] Managed Browser supports opening web content from [Microsoft apps you can use with Microsoft Intune mobile application management policies](../Topic/Microsoft_apps_you_can_use_with_Microsoft_Intune_mobile_application_management_policies.md).

## Create a managed browser policy

1. In the [Microsoft Intune administration console](https://manage.microsoft.com), click **Policy** &gt; **Add Policy**.

2. Configure one of the following **Software** policy types:

   - **Managed Browser Policy (Android 4 and later)**

   - **Managed Browser Policy (iOS 7.1 and later)**

   For more information about how to create and deploy policies, see the [Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md) topic.

3. Use the following table to help you configure the managed browser policy settings:

   |Setting name <br /> <br />|More information <br /> <br />|
   |----------------|--------------------|
   |**Name** <br /> <br />|Enter a unique name for the managed browser policy to help you identify it in the [!INC[wit_nextref](../Token/wit_nextref_md.md)] console. <br /> <br />|
   |**Description** <br /> <br />|Provide a description that gives an overview of the managed browser policy and other relevant information that helps you to locate it. <br /> <br />|
   |**Enable an allow list or block list to restrict the URLs the Managed Browser can open** <br /> <br />|Select one of the following options: <br /> <br /><ul><li>**Allow the managed browser to open only the URLs listed below** – Specify a list of URLs that the managed browser can open. </li><li>**Block the managed browser from opening the URLs listed below** – Specify a list of URLs that the managed browser will be blocked from opening. </li> </ul> **Note:** You cannot include both allowed and blocked URLs in the same managed browser policy. <br />For more information about the URL formats you can specify, see [URL Format for allowed and blocked URLs](../Topic/Manage_Internet_access_using_managed_browser_policies_with_Microsoft_Intune.md#BKMK_URLs) in this topic. <br /> <br />|

4. When you are finished, click **Save Policy**.

The new policy displays in the **Configuration Policies** node of the **Policy** workspace.

## Create a software deployment for the managed browser app
After you have created the managed browser policy, you can then create a software deployment for the managed browser app, and associate it with the managed browser policy you created.

> [!IMPORTANT]
> Managed browser policies are not deployed in the same way as other [!INC[wit_nextref](../Token/wit_nextref_md.md)] polices. This type of policy must be associated with the managed browser software package.

Deploy the app, ensuring that you select the managed browser policy on the **Mobile App Management** page to associate the policy with the app.

For more information about how to deploy apps, see [Deploy apps to mobile devices in Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune.md).

## Security and privacy for the managed browser

- On iOS devices, web sites that users visit that have an expired or untrusted certificate cannot be opened.

- Settings that users make for the built-in browser on their devices are not used by the managed browser. This is because the managed browser does not have access to these settings.

- If you configure the options **Require simple PIN for access** or **Require corporate credentials for access** in a mobile application management policy associated with the managed browser and a user clicks the help link on the authentication page, they can then browse any Internet sites regardless of whether they were added to a block list in the managed browser policy.

- The managed browser can only block access to sites when they are accessed directly. It cannot block access when intermediate services (such as a translation service) are used to access the site.

- To allow authentication, and to ensure that [!INC[wit_nextref](../Token/wit_nextref_md.md)] documentation can be accessed,**&#42;.microsoft.com** is exempt from the allow or block list settings – it is always allowed.

### Turn off usage data
Microsoft automatically collects anonymous data about the performance and use of the managed browser to improve Microsoft products and services, but users can turn off data collection by using the **Usage Data** setting on their device. You have no control over the collection of this data.

## Reference information

### <a name="BKMK_URLs"></a>URL format for allowed and blocked URLs
Use the following information to learn about the allowed formats and wildcards you can use when specifying URLs in the allowed and blocked lists.

- You can use the wildcard symbol ‘**&#42;**’ according to the rules in the permitted patterns list below.

- Ensure that you prefix all URLs with **http** or **https** when entering them into the list.

- You can specify port numbers in the address. If you do not specify a port number, the values used will be:

   - Port 80 for http

   - Port 443 for https

   Using wildcards for the port number is not supported, for example, **http://www.contoso.com:&#42;** and **http://www.contoso.com: /&#42;**

- Use the following table to learn about the permitted patterns you can use when you specify URLs:

   |URL <br /> <br />|Description <br /> <br />|Matches <br /> <br />|Does not match <br /> <br />|
   |-------|---------------|-----------|------------------|
   |http://www.contoso.com <br /> <br />|Matches a single page <br /> <br />|www.contoso.com <br /> <br />|host.contoso.com <br /> <br />www.contoso.com/images <br /> <br />contoso.com/ <br /> <br />|
   |http://contoso.com <br /> <br />|Matches a single page <br /> <br />|contoso.com/ <br /> <br />|host.contoso.com <br /> <br />www.contoso.com/images <br /> <br />www.contoso.com <br /> <br />|
   |http://www.contoso.com/&#42; <br /> <br />|Matches all URLs beginning with www.contoso.com <br /> <br />|www.contoso.com <br /> <br />www.contoso.com/images <br /> <br />www.contoso.com/videos/tvshows <br /> <br />|host.contoso.com <br /> <br />host.contoso.com/images <br /> <br />|
   |http://&#42;.contoso.com/&#42; <br /> <br />|Matches all sub-domains under contoso.com <br /> <br />|developer.contoso.com/resources <br /> <br />news.contoso.com/images <br /> <br />news.contoso.com/videos <br /> <br />|contoso.host.com <br /> <br />|
   |http://www.contoso.com/images <br /> <br />|Matches a single folder <br /> <br />|www.contoso.com/images <br /> <br />|www.contoso.com/images/dogs <br /> <br />|
   |http://www.contoso.com:80 <br /> <br />|Matches a single page, using a port number <br /> <br />|http://www.contoso.com:80 <br /> <br />||
   |https://www.contoso.com <br /> <br />|Matches a single, secure page <br /> <br />|https://www.contoso.com <br /> <br />|http://www.contoso.com <br /> <br />|
   |http://www.contoso.com/images/&#42; <br /> <br />|Matches a single folder and all subfolders <br /> <br />|www.contoso.com/images/dogs <br /> <br />www.contoso.com/images/cats <br /> <br />|www.contoso.com/videos <br /> <br />|

- The following are examples of some of the inputs you cannot specify:

   - &#42;.com

   - &#42;.contoso/&#42;

   - www.contoso.com/&#42;images

   - www.contoso.com/&#42;images&#42;pigs

   - www.contoso.com/page&#42;

   - IP addresses

   - https://&#42;

   - http://&#42;

   - http://www.contoso.com:&#42;

   - http://www.contoso.com: /&#42;

### How conflicts between the allow and block list are resolved
If multiple managed browser policies are deployed to a device and the settings conflict, both the mode (allow or block) and the URL lists are evaluated for conflicts. In case of a conflict, the following behavior applies:

- If the modes in each policy are the same, but the URL lists are different, the URLs will not be enforced on the device.

- If the modes in each policy are different, but the URL lists are the same, the URLs will not be enforced on the device.

- If a device is receiving managed browser policies for the first time and two policies conflict, the URLs will not be enforced on the device. Use the **Policy Conflicts** node of the **Policy** workspace to view the conflicts.

- If a device has already received a managed browser policy and a second policy is deployed with conflicting settings, the original settings remain on the device. Use the **Policy Conflicts** node of the **Policy** workspace to view the conflicts.

## See Also
[Enable access to company resources with Microsoft Intune](http://msdn.microsoft.com/en-us/library/5b090c5a-6f12-4e60-ace0-c9929afaa9a3)

