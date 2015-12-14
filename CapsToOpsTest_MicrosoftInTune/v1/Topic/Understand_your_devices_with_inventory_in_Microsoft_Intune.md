---
description: na
keywords: na
pagetitle: Understand your devices with inventory in Microsoft Intune
search: na
ms.author: f93f38ed286b4cbb94b9b427a0abc63e
ms.date: 2015-11-17
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 312911fe-b963-4949-9911-ae425e0590b2
---
# Understand your devices with inventory in Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] lets you view the inventory of enrolled devices and Windows PCs that run the [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] client software.

## What's collected from enrolled devices?
To view the inventory collected by mobile devices, run the [Mobile Device Inventory Reports](https://technet.microsoft.com/library/dn646977.aspx). [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] collects the following inventory from mobile devices:

|Property <br /> <br />|Exchange ActiveSync <br /> <br />|iOS <br /> <br />|Mac OS X <br /> <br />|Android <br /> <br />|Windows RT and Windows 8.1 <br /> <br />|Windows Phone 8 and Windows Phone 8.1 <br /> <br />|Windows 10 <br /> <br />|Notes <br /> <br />|
|------------|-----------------------|-------|------------|-----------|------------------------------|-----------------------------------------|--------------|---------|
|**Name** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />||
|**Operating System** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />||
|**Manufacturer** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />||
|**Model** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />||
|**Management Channel** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />||
|**AAD Registered** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|No <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />||
|**Compliant** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />||
|**EAS Activated** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|No <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />||
|**EAS Activation ID** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|No <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />||
|**EAS Activation Time** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|No <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />||
|**Management State** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />||
|**Email Address** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />||
|**Exchange ActiveSync ID** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />||
|**Jailbroken or Rooted** <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />||
|**Unique Device ID** <br /> <br />|No <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />||
|**Serial number** <br /> <br />|No <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|No <br /> <br />|Yes <br /> <br />||
|**Total Storage Space** <br /> <br />|No <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|Yes <br /> <br />||
|**Free Storage Space** <br /> <br />|No <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|Yes <br /> <br />||
|**Phone Number** <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|Phone number is masked with &#42; except for the last 4 digits. <br /> <br />|
|**IMEI** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />||
|**MEID** <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />|Mobile Equipment Identifier <br /> <br />|
|**Wi-Fi MAC** <br /> <br />|No <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />||
|**Subscriber Carrier** <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />||
|**Cellular Technology** <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />||
|**Supervised** <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />||
|**Activation Lock State** <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />||
|**Enrolled Date** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />||
|**Last Updated** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />||
|**Ethernet MAC** <br /> <br />|No <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />||
|**Activation Lock Enabled** <br /> <br />|No <br /> <br />|Yes <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />|No <br /> <br />||
|**Encryption Enabled** <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />|Yes <br /> <br />||

## What's collected from Windows PCs
> [!IMPORTANT]
> This section applies only to Windows PCs that run the [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] computer client software.

To view the inventory collected by Windows PCs, run the [Computer Inventory Reports](https://technet.microsoft.com/library/dn646977.aspx). [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] collects the following inventory from Windows PCs:

- **Name**

- **Chassis Type**

- **Manufacturer**

- **Model**

- **Operating System**

- **TPM Version**

- **Total Disk Space**

- **Used Disk Space**

- **Free Disk Space**

- **OS Disk Name**

- **OS Disk Space**

- **OS Disk Free Space**

- **Physical Memory**

- **Processor Name**

- **Processor Architecture**

- **CPU Speed**

- **IP Address**

- **Serial number**

- **Last User to Log On**

- **Assigned User**

- **Last Updated**

## See Also
[Monitoring and reports with Microsoft Intune](../Topic/Monitoring_and_reports_with_Microsoft_Intune.md)

