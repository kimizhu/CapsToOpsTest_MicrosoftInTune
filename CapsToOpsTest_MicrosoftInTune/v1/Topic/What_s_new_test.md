---
description: na
search: na
title: What&#39;s new test
ms.service: na
ms.tgt_pltfrm: na
ms.topic: article
ms.date: na
ms.author: d4484712-0a03-4345-bdeb-64372a73012b
---
# What&#39;s new test

## What's new in Intune
Insert section body here.

### New compliance policy settings (1511) - everything under this section is Karthika's
The following new device health and device property settings are now available:

- **Support for specifying OS version requirements:**

   You can create new compliance rules to set **minimum and maximum OS version** requirements. This allows you to ensure that your end-users are using devices that have the OS versions that are compliant with your requirements.

   **Minimum OS version:** The devices that are used to access your company resources will be required to have at least the minimum version  that you specify. For devices that do not meet the minimum version requirement, a message with instructions on how to upgrade is displayed.

   **Maximum OS version setting:** The devices need access to your company resources will be required to have a version no later than the version you specify. For devices that have an OS version later than the maximum OS version you specified, users will be asked to contact the IT admin. Until there is a change in rule to allow the OS version, this device cannot be used to access company resources.

   Read the [Manage device compliance policies for Microsoft Intune](../Topic/Manage_device_compliance_policies_for_Microsoft_Intune.md) topic to see more details for the new OS version settings.

- **Support for device health attestation:**

   **Windows 10 Device health attestation**  is a way to evaluate the integrity of Windows 10 desktop and mobile devices to make sure that they are not vulnerable to malicious use. For example, the health attestation service can detect whether a device has **Secure Boot** enabled or whether code integrity checks are enforced for running programs.  When you enable the **Require devices to be healthy** setting, the Windows 10 devices will be evaluated for data points gathered by the **Health Attestation Service (HAS)** and collected by Intune.  **Reporting** on Windows 10 health attestation data collected by Intune is available in the **Intune admin console**.

   To make sure the Windows 10 devices  are evaluated for their health status as reported by HAS, you must deploy a conditional access policy for one or more services with the **Require devices to be healthy** setting enabled.

   Read the [Manage device compliance policies for Microsoft Intune](../Topic/Manage_device_compliance_policies_for_Microsoft_Intune.md) topic for more details on the device health setting, collected data points, and  the health attestation report.

   The HAS service details can be found [here](https://msdn.microsoft.com/en-us/library/dn934876.aspx).

### Device management

## Changes and updates to Microsoft Company Portal
The following changes have been made to the company portal apps in this release:

**Android**

**iOS**

## What's coming

## What's new in Intune documentation
**New content**

|||
|-|-|
|Name <br /> <br />|Details <br /> <br />|
|||
|||
**Updated content**

|||
|-|-|
|Name <br /> <br />|Details <br /> <br />|
|||
|||
|||
|||
