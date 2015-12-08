---
description: na
search: na
title: Help with iOS enrollment errors
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.date: 4/30/2015 8:00:00 AM
ms.author: 79a318a2-4407-40ec-b4b0-435e7bd1296a
---
# Help with iOS enrollment errors
This topic helps you to work around iOS enrollment errors.

## iOS enrollment errors
The following table lists errors that users might encounter while enrolling iOS devices. Possible cause and solution details are provided for each error.

|Error message <br /> <br />|Possible cause <br /> <br />|Resolution using [!INC[wit_firstref](../Token/wit_firstref_md.md)] <br /> <br />|Resolution using System Center 2012 R2 Configuration Manager <br /> <br />|
|-----------------|------------------|--------------------------------------------------------------------------|----------------------------------------------------------------|
|DeviceCapReached <br /> <br />|This message indicates that the user has too many mobile devices enrolled already. <br /> <br />|Before the user enrolls another mobile device, they must remove one of their currently enrolled mobile devices from the company portal. <br /> <br />|Before the user enrolls another mobile device, they must remove one of their currently enrolled mobile devices from the company portal. <br /> <br />|
|APNSCertificateNotValid <br /> <br />|The Apple Push Notification Service (APNS) provides a channel to reach out to enrolled iOS devices. If the steps to obtain an APNS certificate were not performed, or the APNS certificate has expired, then enrollment attempts will fail with this message. <br /> <br />|Review the “External dependencies for enrolling iOS devices” section in the document [Set up iOS and Mac management with Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md) <br /> <br />|Review the “External dependencies for enrolling iOS devices” section in the document [Set up iOS and Mac management with Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md) <br /> <br />|
|AccountNotOnboarded <br /> <br />|The Apple Push Notification Service (APNS) provides a channel to reach out to enrolled iOS devices. If the steps to obtain an APNS certificate were not performed then enrollment attempts will fail with this message. <br /> <br />|Review the “External dependencies for enrolling iOS devices” section in the document [Set up iOS and Mac management with Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md) <br /> <br />|Review the “External dependencies for enrolling iOS devices” section in the document [Set up iOS and Mac management with Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md) <br /> <br />|
|DeviceTypeNotSupported <br /> <br />|You may get this message if you attempt to enroll using a non-iOS device. <br /> <br />|Ensure that the device is running iOS version 5.0 or later. <br /> <br />|Ensure that the device is running iOS version 5.0 or later. <br /> <br />|
|UserLicenseTypeInvalid <br /> <br />|Before users are able to enroll their devices, they must be members of the appropriate user group. This message indicates that the user has the wrong license type for the designated mobile device management authority. For example, if [!INC[wit_firstref](../Token/wit_firstref_md.md)] has been designated as your mobile device management authority, and the user is using a System Center 2012 R2 Configuration Manager license, you will receive this error. <br /> <br />|Review the “Provision users for device enrollment” section in the document [Set up iOS and Mac management with Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md) <br /> <br />|Review the “Provision users for device enrollment” section in the document [Set up iOS and Mac management with Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md) <br /> <br />|
|MdmAuthorityNotDefined <br /> <br />|This message indicates that the mobile device management authority has not been designated in [!INC[wit_firstref](../Token/wit_firstref_md.md)]. <br /> <br />|Review the “Set the Mobile Device Management Authority for Microsoft Intune” section in the document [Set up iOS and Mac management with Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md) <br /> <br />|Review the “Set the Mobile Device Management Authority for Microsoft Intune” section in the document [Set up iOS and Mac management with Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md) <br /> <br />|
