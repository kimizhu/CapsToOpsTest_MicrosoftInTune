---
description: na
search: na
title: Configure access to corporate email using email profiles with Microsoft Intune
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.date: 2015-11-17
ms.author: 03258b9b-2cea-4654-ab05-a27214174f4b
---
# Configure access to corporate email using email profiles with Microsoft Intune
Email profiles in [!INC[wit_firstref](../Token/wit_firstref_md.md)] help you create, deploy and monitor Exchange ActiveSync email settings on devices. This lets user’s access corporate email on their personal devices without any required setup on their part.

You can use email profiles to configure the following device types:

- Devices that run Windows Phone 8 and later

- Devices that run iOS 7.1 and later

- Devices that run Samsung KNOX Standard (4.0 and later)

- Devices that run Windows 10 desktop, Windows 10 Mobile, and later

In addition to configuring an email account on the device, you can also configure synchronization settings such as how much email to synchronize, and depending on the device type, the content types to synchronize.

> [!IMPORTANT]
> Whenever possible, choose the most secure options that your email infrastructure and client operating systems can support. Email profiles provide a convenient method to centrally distribute and manage email settings that your devices already support. [!INC[wit_nextref](../Token/wit_nextref_md.md)] does not add email functionality.

## How email profiles are secured
Email profiles can be secured using one of two methods:

### Certificates
When you create the email profile, you choose a SCEP certificate profile that you have previously created in [!INC[wit_nextref](../Token/wit_nextref_md.md)]. This is known as the identity certificate and is used to authenticate against a trusted certificate profile (or a root certificate) you created to establish that the user’s device is allowed to connect. The trusted certificate is deployed to the computer that authenticates the email connection, typically, the Exchange server.

For more information about how to create and use certificate profiles in [!INC[wit_nextref](../Token/wit_nextref_md.md)], see [Enable access to company resources using certificate profiles with Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).

### Username and password
The user authenticates to the Exchange server by providing their username and password.

The password is not contained in the email profile, so the user will need to supply this when they connect to email.

### Create an email profile

1. In the [Microsoft Intune administration console](https://manage.microsoft.com), click **Policy** &gt; **Add Policy**.

2. Configure one of the following policy types:

   - **Email Profile for Samsung KNOX Standard (4.0 and later)**

   - **Email Profile (iOS 7.1 and later)**

   - **Email Profile (Windows Phone 8 and later)**

   - **Email Profile (Windows 10 Desktop and Mobile and later)**

   You can only create and deploy a custom email profile policy. Recommended settings are not available.

   For more information about how to create and deploy policies, see the [Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md) topic.

3. Use the following table to help you configure Samsung KNOX email profile settings:

   |Setting name <br /> <br />|More information <br /> <br />|
   |----------------|--------------------|
   |**Name** <br /> <br />|Enter a unique name for the email profile. <br /> <br />|
   |**Description** <br /> <br />|Provide a description that gives an overview of the email profile and other relevant information that helps you to locate it. <br /> <br />|
   |**Host** <br /> <br />|Specify the hostname of your company Exchange Server that hosts Exchange ActiveSync services. <br /> <br />|
   |**Account name** <br /> <br />|Specify the display name for the email account as it will appear to users on their devices. <br /> <br />|
   |**Username** <br /> <br />|Select how the username for the email account will be obtained: <br /> <br /><ul><li>For an On-premises Exchange server, select **Username**. </li><li>For Office 365, select  **User Principal Name** </li> </ul>|
   |**Email address** <br /> <br />|Select how the email address for the user on each device is generated: <br /> <br /><ul><li>**Primary SMTP Address** - Use the users primary SMTP address to log onto Exchange. </li><li>**User Principal Name** - Use the full user principal name as the email address. </li> </ul>|
   |**Authentication method** <br /> <br />|Select the authentication method used by the email profile: <br /> <br /><ul><li>**Username and Password** </li><li>**Certificates** </li> </ul>|
   |**Select a client certificate for client authentication (Identity Certificate)** <br /> <br />|Select the client SCEP certificate that you previously created that will be used to authenticate the Exchange connection. For more information about how to use certificate profiles in [!INC[wit_nextref](../Token/wit_nextref_md.md)], see [Enable access to company resources using certificate profiles with Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md). **Note:** This option is displayed only when the authentication method is **Certificates**. <br />|
   |**Use S/MIME** <br /> <br />|Send outgoing email using S/MIME encryption. <br /> <br />|
   |**Signing certificate** <br /> <br />|Select the signing certificate that will be used to sign outgoing email. **Note:** This option is displayed only when you select **Use S/MIME**. <br />|
   |**Number of days of email to synchronize** <br /> <br />|From the drop-down list, select the number of days of email that you want to synchronize or select **Unlimited** to synchronize all available email. <br /> <br />|
   |**Sync schedule** <br /> <br />|Select the schedule by which devices will synchronize data from the Exchange Server. You can also select **As Messages arrive** which synchronizes data as soon as it arrives, or **Manual**, where the user of the device must initiate the synchronization. <br /> <br />|
   |**Use SSL** <br /> <br />|Use Secure Sockets Layer (SSL) communication when sending emails, receiving emails, and communicating with the Exchange Server. **Note:** For devices that run Samsung KNOX 4.0 or later, you must export your Exchange Server’s SSL certificate and deploy it as an Android Trusted Certificate Profile in [!INC[wit_nextref](../Token/wit_nextref_md.md)]. [!INC[wit_nextref](../Token/wit_nextref_md.md)] does not support accessing this certificate if it is installed on the Exchange Server by other means. <br />|
   |**Content type to synchronize** <br /> <br />|Select the content types that you want to synchronize to devices. Choose from: <br /> <br /><ul><li>**Email** </li><li>**Contacts** </li><li>**Calendar** </li><li>**Tasks** </li><li>**Notes** </li> </ul>|
   Use the following table to help you configure iOS email profile settings:

   |Setting name <br /> <br />|More information <br /> <br />|
   |----------------|--------------------|
   |**Name** <br /> <br />|Enter a unique name for the email profile. <br /> <br />|
   |**Description** <br /> <br />|Provide a description that gives an overview of the email profile and other relevant information that helps you to locate it. <br /> <br />|
   |**Host** <br /> <br />|Specify the hostname of your company Exchange Server that hosts Exchange ActiveSync services. <br /> <br />|
   |**Account name** <br /> <br />|Specify the display name for the email account as it will appear to users on their devices. <br /> <br />|
   |**Username** <br /> <br />|Select how the user name for the email account on each device is generated. You can select one of the following options from the drop-down list: <br /> <br /><ul><li>**Primary SMTP Address** - Use the users primary SMTP address to log onto Exchange. </li><li>**User Principal Name** - Use the full user principal name to log onto Exchange. </li> </ul>|
   |**Email address** <br /> <br />|Select how the email address for the user on each device is generated. You can select one of the following options from the drop-down list: <br /> <br /><ul><li>**Primary SMTP Address** - Use the users primary SMTP address to log onto Exchange. </li><li>**User Principal Name** - Use the full user principal name as the email address. </li> </ul>|
   |**Authentication method** <br /> <br />|Select the authentication method used by the email profile: <br /> <br /><ul><li>**Username and Password** </li><li>**Certificates** </li> </ul>|
   |**Select a client certificate for client authentication (Identity Certificate)** <br /> <br />|Select the client SCEP certificate that you previously created that will be used to authenticate the Exchange connection. For more information about how to use certificate profiles in [!INC[wit_nextref](../Token/wit_nextref_md.md)], see [Enable access to company resources using certificate profiles with Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md). **Note:** This option is displayed only when the authentication method is **Certificates**. <br />|
   |**Use S/MIME** <br /> <br />|Send outgoing email using S/MIME encryption. <br /> <br />|
   |**Signing certificate** <br /> <br />|Optionally, select the signing certificate that will be used to sign outgoing email. **Note:** This option is displayed only when you select **Use S/MIME**. <br />|
   |**Number of days of email to synchronize** <br /> <br />|From the drop-down list, select the number of days of email that you want to synchronize or select **Unlimited** to synchronize all available email. <br /> <br />|
   |**Use SSL** <br /> <br />|Use Secure Sockets Layer (SSL) communication when sending emails, receiving emails, and communicating with the Exchange Server. <br /> <br />|
   |**Allow messages to be moved to other email accounts** <br /> <br />|Allow users to move email messages between different accounts they have configured on their device. <br /> <br />|
   |**Allow email to be sent from third-party applications** <br /> <br />|Allow users to send email from apps other than the default email app. <br /> <br />|
   |**Synchronize recently used email addresses** <br /> <br />|Synchronize the list of email addresses that have been recently used on the device. <br /> <br />|
   Use the following table to help you configure Windows Phone email profile settings:

   |Setting name <br /> <br />|More information <br /> <br />|
   |----------------|--------------------|
   |**Name** <br /> <br />|Enter a unique name for the email profile. <br /> <br />|
   |**Description** <br /> <br />|Provide a description that gives an overview of the email profile and other relevant information that helps you to locate it. <br /> <br />|
   |**Host** <br /> <br />|Specify the hostname of your company Exchange Server that hosts Exchange ActiveSync services. <br /> <br />|
   |**Account name** <br /> <br />|Specify the display name for the email account as it will appear to users on their devices. <br /> <br />|
   |**Username** <br /> <br />|Select how the user name for the email account on each device is generated. You can select one of the following options from the drop-down list: <br /> <br /><ul><li>**Primary SMTP Address** - Use the users primary SMTP address to log onto Exchange. </li><li>**User Principal Name** - Use the full user principal name to log onto Exchange. </li> </ul>|
   |**Email Address** <br /> <br />|Select how the email address for the user on each client device is generated. You can select one of the following options from the drop-down list: <br /> <br /><ul><li>**Primary SMTP Address** Use the users primary SMTP address to log onto Exchange. </li><li>**User Principal Name** Use the full user principal name as the email address. </li> </ul>|
   |**Number of days of email to synchronize** <br /> <br />|From the drop-down list, select the number of days of email that you want to synchronize or select **Unlimited** to synchronize all available email. <br /> <br />|
   |**Sync Schedule** <br /> <br />|Select the schedule by which devices will synchronize data from the Exchange Server. You can also select **As Messages arrive** which synchronizes data as soon as it arrives, or **Manual**, where the user of the device must initiate the synchronization. <br /> <br />|
   |**Use SSL** <br /> <br />|Use Secure Sockets Layer (SSL) communication when sending emails, receiving emails, and communicating with the Exchange Server. <br /> <br />|
   |**Content type to synchronize** <br /> <br />|Select the content types that you want to synchronize to devices. Choose from: <br /> <br /><ul><li>**Email** </li><li>**Contacts** </li><li>**Calendar** </li><li>**Tasks** </li> </ul>|
   > [!IMPORTANT]
   > If you have deployed an email profile and then wish to change the values for **Exchange ActiveSync host** or **Email address**, you must delete the existing email profile and create a new one with the required values.

4. When you are finished, click **Save Policy**.

The new policy displays in the **Configuration Policies** node of the **Policy** workspace.

### Deploy an email profile

1. Deploy the email profile to one or more groups of users or devices in your organization.

For more information about how to deploy policies, see [Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

A status summary and alerts on the **Overview** page of the **Policy** workspace identify issues with the policy that require your attention. Additionally, a status summary appears in the **Dashboard** workspace.

> [!NOTE]
> If you want to remove an email profile from a device, edit the deployment and remove any groups of which the device is a member.

## Next Steps
After successful deployment, user’s devices will be provisioned with the correct settings to access corporate email.

## See Also
[Enable and help secure access to company resources using Windows Intune](http://msdn.microsoft.com/en-us/library/5b090c5a-6f12-4e60-ace0-c9929afaa9a3)

