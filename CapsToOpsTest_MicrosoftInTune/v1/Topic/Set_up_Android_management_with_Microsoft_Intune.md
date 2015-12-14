---
description: na
keywords: na
pagetitle: Set up Android management with Microsoft Intune
search: na
ms.author: f93f38ed286b4cbb94b9b427a0abc63e
ms.date: 2015-11-17
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dbe5cad1-3e0d-41a9-966b-738156089700
---
# Set up Android management with Microsoft Intune
Android mobile devices allow users to enroll using the Company Portal app available from Google Play. To let users enroll their devices in [!INC[wit_nextref](../Token/wit_nextref_md.md)] complete the following.

## Set up Android mobile devices with Microsoft Intune

1. **Set up [!INC[wit_nextref](../Token/wit_nextref_md.md)]**
   If you haven’t already, prepare for mobile device management by  [setting the mobile device management authority](https://technet.microsoft.com/library/mt346013.aspx) as **Microsoft Intune**.

2. **Add Intune users**
   The mobile device owner must be added to the account portal before devices can be enrolled. Log in to the [Microsoft Intune Account Portal](http://go.microsoft.com/fwlink/?LinkId=698854), click **Add users**, and select an option:

   - **User**: To add a single user select **New** &gt; **User** and enter **Details**, **Assign roles**, **Set user location**, and then assign the user to a **Group**.

   - **Bulk add**: Create a .csv file (see samples files provided) and import it into the account portal. Specify roles, location, and group, and then create the accounts. Sample and blank .csv files can be downloaded from the account portal.

   You can also enable Active Directory or Azure Active Directory synchronization. For more information about integrating other Azure Active Directory users with Intune, see [Directory synchronization roadmap](http://go.microsoft.com/fwlink/?LinkId=511540) or click **Other ways to add users** in the account portal.

3. **Create groups**  (Optional)
   Groups give flexibility for managing devices and users. You can set up groups to suit your organizational needs by geographic location, department, or hardware characteristics, for example.   See [Use groups to manage users and devices with Microsoft Intune](../Topic/Use_groups_to_manage_users_and_devices_with_Microsoft_Intune.md).

4. **Add policies for devices** (Optional)
   Policies are groups of settings that control features on devices. Most MDM policies are platform specific. You create policies using templates  containing recommended or customized settings, and then deploy them to groups. See [Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

5. **Set device enrollment limit** (Optional) 
   To limit the number of mobile devices a user can enroll, log in to the [Microsoft Intune administration console](http://manage.microsoft.com), click **Admin** &gt; **Mobile Device Management** &gt; **Enrollment rules**. Select the maximum number of devices a user can enroll and then click **Save**.

6. **Set Company Portal settings** 
    You can customize the Intune Company Portal for your company. In the [Microsoft Intune administration console](http://manage.microsoft.com) click **Admin** &gt; **Company Portal**. Configure the following

   - **Company Name**

   - **IT department contact name**

   - **IT department phone number**

   - **Additional information**

   - **Company privacy statement URL**

   - **Support website URL (not displayed)**

   - **Website name**

7. [!INC[CPEnrollmentTermsAndConditions](../Token/CPEnrollmentTermsAndConditions_md.md)]

8. **Tell users how to get access to company resources with the company portal**
   Your users will need to know how to enroll their devices and what to expect once they're brought into management. [What to tell your end users about using Microsoft Intune](../Topic/What_to_tell_your_end_users_about_using_Microsoft_Intune.md)

## See Also
[Get ready to enroll devices in Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md)

