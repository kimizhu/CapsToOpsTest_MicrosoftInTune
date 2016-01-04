---
description: na
keywords: na
pagetitle: Use conditional access with Intune by itself
search: na
ms.date: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1d876fb1-a857-4350-8970-3eb38c483111
ms.author: 70da87b7-2f4c-4e11-98d3-a3b38e8154d2
---
# Use conditional access with Intune by itself
You can use conditional access in Intune to help secure email and email data depending on the conditions you specify. Conditional access lets you manage access to Microsoft Exchange Server on-premises and Exchange Online.

Similar to how you [Use conditional access with Intune and Configuration Manager](../Topic/Use_conditional_access_with_Intune_and_Configuration_Manager.md), you  implement conditional access in Intune by itself by configuring two policy types:

- **Compliance policies** are optional policies you can deploy to users and devices and evaluate settings like passcode and encryption.
   If no compliance policy is deployed to a device, then any applicable conditional access policies will treat the device as compliant.

- **Conditional access policies** are configured for a particular service, and define rules such as which Azure Active Directory security user groups or Intune user groups will be targeted and how devices that cannot enroll with Intune will be managed.

Unlike other Intune policies, you do not deploy conditional access policies. Instead, you configure these once, and they apply to all targeted users.

When devices do not meet the conditions you configure, the user is guided through the process of enrolling the device and fixing the issue that prevents the device from being compliant.

> [!TIP]
> Get a downloadable copy of this entire topic at the [TechNet Gallery](https://gallery.technet.microsoft.com/Deploying-Enterprise-16499404).

## Prerequisites
You can control access to Exchange Online and Exchange on-premises from the following mail apps:

- The built-in app for Android 4.0 and later, Samsung Knox 4.0 Standard and later

- The built-in app for iOS 7.1 and later

- The built-in app for Windows Phone 8.1 and later

- The mail application on Windows 8.1 and later

- The Microsoft Outlook app for Android and iOS (for Exchange Online only)

Before you start using conditional access, ensure that you have the correct requirements in place:

### For Exchange Server on-premises
Conditional access to Exchange on-premises supports:

- Windows 8 and later (when enrolled with Intune)

- Windows Phone 8 and later

- Any iOS device that uses an Exchange ActiveSync (EAS) email client

- Android 4 and later

Additionally:

- Your Exchange version must be Exchange 2010 or later. Exchange server Client Access Server (CAS) array is supported.

   > [!TIP]
   > If your Exchange environment is in a CAS server configuration, then you must install the on-premises Exchange connector on any one of the CAS servers.

- Exchange ActiveSync can be configured with certificate based authentication, or user credential entry.

- You must use the **on-premises Exchange connector** which connects Intune to Microsoft Exchange Server on-premises. This lets you manage devices through the Intune console (see [Mobile device management with Exchange ActiveSync and Microsoft Intune](https://technet.microsoft.com/en-us/library/dn646988.aspx)).

> [!IMPORTANT]
> Make sure that you are using the latest version of the on-premises Exchange connector. The on-premise Exchange connector available to you in the Intune console is specific to your Intune tenant and cannot be used with any other tenant. You should also ensure that the exchange connector for your tenant is installed on exactly one machine and not on multiple machines.

### For Exchange Online
Insert subsection body here.

## Deployment Steps for using Exchange on-premises with Intune

### Step 1: Install and configure the Microsoft Intune on-premises Exchange Server connector.

### Step 2: Identify users who will be impacted by conditional access policy.

### Step 3: Create compliance policies and deploy to users.

### Step 4: Configure user groups for the conditional access policy.

### Step 5: Configure the conditional access policy for Exchange on-premises.

## Deployment Steps for using Exchange Online with Intune

### Step 1: Evaluate the effect of the conditional access policy.

### Step 2: Create compliance policies and deploy to users.

### Step 3: Configure user groups for the conditional access policy.

### Step 4: Configure the conditional access policy for Exchange Online

## Reporting

### Monitor the compliance and conditional access policies

### View devices that do not conform to a compliance policy

