---
description: na
keywords: na
pagetitle: Get started with mobile app management policies in the Azure portal
search: na
ms.author: fb8a7802-3b27-41b8-82f3-31bfdcf49ff2
ms.date: 2015-11-17
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7e6a85e7-e007-41b6-9034-64d77f547b87
---
# Get started with mobile app management policies in the Azure portal
This topic tells you what you need to get started creating mobile app management policies (MAM) in the Azure portal.

**In this topic**

[Supported apps](#bkmk_supportedapps)

[Supported  platforms](#bkmk_supportedplatforms)

[What you need to get started](#bkmk_Prereqs)

[Set up the prerequisites](#bkmk_prereqshowto)

[Accessing the Azure preview portal](#bkmk_azureportal)

[Next steps](#bkmk_nextsteps)

## <a name="bkmk_supportedplatforms"></a>Supported  platforms

- iOS 7.1 or later

- Android 4 or later

## <a name="bkmk_supportedapps"></a>Supported apps
**iOS:** Microsoft Word, Excel, PowerPoint,  and OneDrive

**Android:** OneDrive

## <a name="bkmk_Prereqs"></a>What you need to get started
Before you start, you'll need the following:

- A subscription to [!INC[wit_firstref](../Token/wit_firstref_md.md)].    End-users need [!INC[wit_nextref](../Token/wit_nextref_md.md)] licenses to get apps with MAM policy.

- An Office 365 (O365) subscription and Azure Active Directory (Azure AD) to create users and assign [!INC[wit_nextref](../Token/wit_nextref_md.md)] licenses.  Azure AD authenticates the user when the end-user launches the app and enters their work credentials.

   > [!NOTE]
   > If you are setting up users using the [!INC[wit_nextref](../Token/wit_nextref_md.md)] console, be aware that the MAM policy configuration is moving to the Azure portal going forward and to use this portal, you need to set up Azure AD user groups using the Office 365 portal.

## <a name="bkmk_prereqshowto"></a>Set up the prerequisites
The following table lists the role and permissions you can assign to admin users

|||
|-|-|
|**Role** <br /> <br />|**Permissions** <br /> <br />|
|Global administrator (O365 portal) <br /> <br />|<ul><li>Access to O365 portal </li><li>Access to  Azure AD portal </li><li>Access to Azure preview portal (can do both role management and mobile app management tasks. </li> </ul>|
|Owner role (Azure preview portal) <br /> <br />|<ul><li>Access to Azure preview portal (can do both role management and mobile app management tasks. </li> </ul>|
|Contributor role (Azure preview portal) <br /> <br />|<ul><li>Access to Azure preview portal (can only do the mobile app management tasks. </li> </ul>|

#### Create users and assign [!INC[wit_nextref](../Token/wit_nextref_md.md)] licenses

1. You   already have an [!INC[wit_nextref](../Token/wit_nextref_md.md)] subscription if you are currently using [!INC[wit_nextref](../Token/wit_nextref_md.md)] to manage your devices.  You also have an [!INC[wit_nextref](../Token/wit_nextref_md.md)] subscription if you have purchased an EMS license. If you are trying [!INC[wit_nextref](../Token/wit_nextref_md.md)] to check out the MAM capabilities, you can get a trial account [here](http://www.microsoft.com/en-us/server-cloud/products/microsoft-intune/).

   To check if you have an [!INC[wit_nextref](../Token/wit_nextref_md.md)] subscription, on the Office portal, go to Billing page.  You should see [!INC[wit_nextref](../Token/wit_nextref_md.md)] as **Active** under subscriptions.

2. Sign in to the   [the Office portal](http://portal.office.com) with your admin credentials.

3. Navigate to the **Active Users** page to add users and assign [!INC[wit_nextref](../Token/wit_nextref_md.md)] licenses.

   ![](../Image/AppManagement/OfficePortal_AddUsers.png)

4. To give a user the ability to access the Office portal, the Azure AD portal and the Azure preview portal, assign the **Global administrator role** to the user.

   ![](../Image/AppManagement/OfficePortal_AddRoletoUser.png)

5. MAM policies are deployed to user groups in Azure Active Directory. To create user groups you want to use for your MAM policies, navigate to the **Groups** page on the **Office  portal** and click the **+** icon to create a new security group.  Type a name and description and click **Create**. When the group is created, you can add user to the group by clicking **Edit members** on the newly created security group. The security group is created in Azure Active Directory.

   ![](../Image/AppManagement/OfficePortal_CreateGroups.png)

## <a name="bkmk_azureportal"></a>Accessing the Azure preview portal
The **Azure preview portal** allows you create app policies, deploy it the policy to users, and monitor the status of your deployment.

#### To get started using the portal

1. Go the [Azure preview portal](https://portal.azure.com) and sign in with  your [!INC[wit_nextref](../Token/wit_nextref_md.md)] credentials.

   ![](../Image/AppManagement/AzurePortal_MAMSigninPage.png)

2. Once you are successfully signed in, you will see the **Start** page or **home** page. The **Start** page or the home page comes with a set of default tiles that you can remove and add new ones to customize the page.

   ![](../Image/AppManagement/AzurePortal_MAMStartboard_NoMAM.png)

3. From the **Browse** menu, find **Intune**.![](../Image/AppManagement/AzurePortal_MAM_Browse_Intune.png)

4. Click **Intune &gt; Intune mobile application management &gt; Settings**.

   ![](../Image/AppManagement/AzurePortal_MAM_Mainblade.png)

   > [!TIP]
   > To pin a blade to the **Start** page, you can use the **pin** option on the blade.  Click the pin icon on the **Intune mobile application management blade**, to pin it to the **Start** page.

   ![](../Image/AppManagement/AzurePortal_MAM_PinBladeAction.png)

   ![](../Image/AppManagement/AzurePortal_MAM_Startboard_withMAM.png)

**Global administrators** have access to the Azure portal.  If you want other admin users to be able to configure policies, and do other mobile app management tasks, you can assign the **contributor role** to the user as described below:

#### Assign contributor role to a user

1. On the **Settings** blade,  from the **Resource management**section, click **Users**.

   ![](../Image/AppManagement/AzurePortal_MAM_AddUsers.png)

2. Click **Add** to open the **Add access** blade.

3. Click **Select a role**, then **Contributor role**.

   ![](../Image/AppManagement/AzurePortal_MAM_AddRole.png)

4. Once you have selected the role, click **Add user**, and search for the user by the user name or email address. The users you see on this list are the first 1000 users you previously created in Azure AD using the Office portal. Click **Ok** on the **Add access** blade to save and assign the role to the user.

   ![](../Image/AppManagement/AzurePortal_MAM_AddusertoRole.png)

   > [!IMPORTANT]
   > If you select a user who does not have an [!INC[wit_nextref](../Token/wit_nextref_md.md)] license assigned to them, they will not be able to access the portal.

## <a name="bkmk_nextsteps"></a>Next steps
[Create and deploy mobile app management policies with Microsoft Intune](../Topic/Create_and_deploy_mobile_app_management_policies_with_Microsoft_Intune.md)

## See Also
[Configure data loss prevention app policies with Microsoft Intune](../Topic/Configure_data_loss_prevention_app_policies_with_Microsoft_Intune.md)

