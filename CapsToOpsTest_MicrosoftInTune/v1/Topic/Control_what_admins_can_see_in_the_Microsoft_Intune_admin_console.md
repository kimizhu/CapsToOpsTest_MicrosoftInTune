---
description: na
keywords: na
pagetitle: Control what admins can see in the Microsoft Intune admin console
search: na
ms.author: dbdc710f437843008017318979c6adba
ms.date: 2015-08-01
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e0783eaa-67dc-410e-9e80-4d3aa72f36d8
---
# Control what admins can see in the Microsoft Intune admin console
[!INC[wit_nextref](../Token/wit_nextref_md.md)] provides the ability to filter the admin console view to allow users to access only the items you want them to see. For example, you might want to allow only admin console operators to be able to update malware definitions, or reset the passcode on devices. This is accomplished by using preset **designations** that you assign to specific users. When these users access the admin console, they only see items specific to their designation.

Use this feature to help you assign administration tasks to staff while still ensuring the security of your [!INC[wit_nextref](../Token/wit_nextref_md.md)] data.

## How to assign a designation to a user

1. In the [Microsoft Intune administration console](https://manage.microsoft.com), click **Admin** &gt; **Service Administrators**.

2. From the list of service administrators, choose the user whose designation you want to change, and then click **Manage Access**.

3. In the **Manage Access** dialog box, choose the level of access that you want to give the selected user. You can choose from:

   - **Full access**

   - **Read only access**

   Additionally, you can choose from one of the following designations that provide custom levels of access to the [!INC[wit_nextref](../Token/wit_nextref_md.md)] admin console:

   |Designation <br /> <br />|User can: <br /> <br />|
   |---------------|-------------|
   |**Helpdesk - Groups Node** <br /> <br />|<ul><li>See lists of users and devices (the user cannot use filters to modify the view. However, you can use group filtering to modify what the user can see). For more information, see [Use groups to manage users and devices with Microsoft Intune](../Topic/Use_groups_to_manage_users_and_devices_with_Microsoft_Intune.md). </li><li>Print the list of users and devices. </li><li>Export the list of users and devices </li><li>View the properties of a user or device. </li><li>Perform the following remote tasks: <br /> <br /><ul><li>Run a full malware scan </li><li>Run a quick malware scan </li><li>Restart a computer </li><li>Update malware definitions </li><li>Refresh policies </li><li>Refresh inventory </li><li>Remote lock a device </li><li>Passcode reset </li> </ul> </li> </ul>|

When the user you configured next opens the [!INC[wit_nextref](../Token/wit_nextref_md.md)] admin console, they will be given the level of access you specified.

## See Also
[Technical reference for Microsoft Intune](../Topic/Technical_reference_for_Microsoft_Intune.md)

