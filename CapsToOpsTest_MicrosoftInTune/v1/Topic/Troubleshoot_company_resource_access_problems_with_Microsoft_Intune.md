---
description: na
keywords: na
pagetitle: Troubleshoot company resource access problems with Microsoft Intune
search: na
ms.author: dbdc710f437843008017318979c6adba
ms.date: 2015-08-01
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 40622ced-6029-4abf-873e-b51d2b51934c
---
# Troubleshoot company resource access problems with Microsoft Intune
Use the information in this topic to help you troubleshoot problems when a [!INC[wit_firstref](../Token/wit_firstref_md.md)] action returns an error code.

If this information does not solve your problem, see [How to get support for Microsoft Intune](../Topic/How_to_get_support_for_Microsoft_Intune.md) to find more ways to get help.

## Error codes related to company resource access

### Status codes for MDM managed Windows devices

|Status code <br /> <br />|Error message <br /> <br />|What to do <br /> <br />|
|---------------|-----------------|--------------|
|10 (APP_CI_ENFORCEMENT_IN_PROGRESS) <br /> <br />|Installation in progress <br /> <br />||
|20 (APP_CI_ENFORCEMENT_IN_PROGRESS_WAITING_CONTENT) <br /> <br />|Waiting for content <br /> <br />||
|30 (APP_CI_ENFORCEMENT_ERROR_RETRIEVING_CONTENT) <br /> <br />|Retrieving content <br /> <br />|Probable Cause: Job status 30 indicates that a user download of an app failed. <br /> <br />Likely causes for this may be: <br /> <br />The device lost Internet connectivity while the download was in progress. <br /> <br />The certificate issued to the device at the time of enrollment may have expired. <br /> <br />Mitigation: <br /> <br />Launch the Company Apps app from Control Panel on the device to confirm that the device certificate hasn’t expired; if it has then you will need to re-enroll the device. <br /> <br />Confirm that the device is connected to the Internet and try to request the app again. <br /> <br />|
|40 (APP_CI_ENFORCEMENT_IN_PROGRESS_CONTENT_DOWNLOADED) <br /> <br />|Content download complete <br /> <br />||
|50 (APP_CI_ENFORCEMENT_IN_PROGRESS_INSTALLING) <br /> <br />|Installation in progress <br /> <br />||
|60 (APP_CI_ENFORCEMENT_ERROR_INSTALLING) <br /> <br />|Installation ​Error occurred <br /> <br />|The app installation failed after download. <br /> <br />The code signing certificate with which app was signed is not present on the device. <br /> <br />A framework dependency on which the application depends upon is not found installed on the device. <br /> <br />Ensure that the code signing certificate with which your app was signed is present on the device and confirm with the admin that such a certificate was targeted for all enterprise enrolled Windows RT devices. <br /> <br />In case the installation failure is due to a missing framework dependency, the admin will have to re-publish the application again packaging the framework along with the application package. <br /> <br />The application package downloaded isn’t a valid package, may have been corrupted, or may not be compatible with the OS version on the device. <br /> <br />|
|70 (APP_CI_ENFORCEMENT_SUCCEEDED) <br /> <br />|Installation Success <br /> <br />||
|80 (APP_CI_ENFORCEMENT_IN_PROGRESS) <br /> <br />|Uninstall in progress <br /> <br />||
|90 (APP_CI_ENFORCEMENT_ERROR) <br /> <br />|Uninstall Error occurred <br /> <br />||
|100 (APP_CI_ENFORCEMENT_SUCCEEDED) <br /> <br />|Uninstall Success <br /> <br />||
|110 (APP_CI_ENFORCEMENT_ERROR) <br /> <br />|Content hash mismatch <br /> <br />||
|120 (APP_CI_ENFORCEMENT_ERROR) <br /> <br />|SLK / side loading not enabled <br /> <br />||
|130 (APP_CI_ENFORCEMENT_ERROR) <br /> <br />|MSADP license install failed <br /> <br />||
|No status (APP_CI_ENFORCEMENT_UNKNOWN) <br /> <br />|n/a <br /> <br />|The status is currently unknown. <br /> <br />|

### Company resource access (common errors)

|Status code <br /> <br />|Hexadecimal error code <br /> <br />|Error message <br /> <br />|
|---------------|--------------------------|-----------------|
|-2016281101 <br /> <br />|0x87D1FDF3 <br /> <br />|MDM CRP request not found <br /> <br />|
|-2016281102 <br /> <br />|0x87D1FDF2 <br /> <br />|NDES URL not found <br /> <br />|
|-2016281103 <br /> <br />|0x87D1FDF1 <br /> <br />|MDM CRP certificate info not found <br /> <br />|
|-2016281104 <br /> <br />|0x87D1FDF0 <br /> <br />|MDM CI certificate info not found <br /> <br />|
|-2016281105 <br /> <br />|0x87D1FDEF <br /> <br />|Failed to evaluate the Rule <br /> <br />|
|-2016281106 <br /> <br />|0x87D1FDEE <br /> <br />|Not applicable because it lost in conflict resolution <br /> <br />|
|-2016281107 <br /> <br />|0x87D1FDED <br /> <br />|Unsupported setting discovery source <br /> <br />|
|-2016281108 <br /> <br />|0x87D1FDEC <br /> <br />|Referenced setting not found in CI <br /> <br />|
|-2016281109 <br /> <br />|0x87D1FDEB <br /> <br />|Data type conversion failed <br /> <br />|
|-2016281110 <br /> <br />|0x87D1FDEA <br /> <br />|Invalid parameter to CIM setting <br /> <br />|
|-2016281111 <br /> <br />|0x87D1FDE9 <br /> <br />|Not applicable for this device <br /> <br />|
|-2016281112 <br /> <br />|0x87D1FDE8 <br /> <br />|Remediation failed <br /> <br />|
|-2016330905 <br /> <br />|0x87D13B67 <br /> <br />|The app state is unknown <br /> <br />|
|-2016330906 <br /> <br />|0x87D13B66 <br /> <br />|The app is managed, but has been removed by the user <br /> <br />|
|-2016330907 <br /> <br />|0x87D13B65 <br /> <br />|The device is redeeming the redemption code <br /> <br />|
|-2016330908 <br /> <br />|0x87D13B64 <br /> <br />|The app install has failed <br /> <br />|
|-2016330909 <br /> <br />|0x87D13B63 <br /> <br />|The user rejected the offer to update the app <br /> <br />|
|-2016330910 <br /> <br />|0x87D13B62 <br /> <br />|The user rejected the offer to install the app <br /> <br />|
|-2016330911 <br /> <br />|0x87D13B61 <br /> <br />|The user has installed the app before managed app installation could take place <br /> <br />|
|-2016330912 <br /> <br />|0x87D13B60 <br /> <br />|The app is scheduled for installation, but needs a redemption code to complete the transaction <br /> <br />|
|-2016341109 <br /> <br />|0x87D1138B <br /> <br />|iOS device has returned an error <br /> <br />|
|-2016341110 <br /> <br />|0x87D1138A <br /> <br />|iOS device has rejected the command due to incorrect format <br /> <br />|
|-2016341111 <br /> <br />|0x87D11389 <br /> <br />|iOS device has returned an unexpected Idle status <br /> <br />|
|-2016341112 <br /> <br />|0x87D11388 <br /> <br />|iOS device is currently busy <br /> <br />|

### Errors returned by iOS devices

|Status code <br /> <br />|Hexadecimal error code <br /> <br />|Error message <br /> <br />|
|---------------|--------------------------|-----------------|
|-2016299111 <br /> <br />|0x87D1B799 <br /> <br />|Internal error <br /> <br />|
|-2016299112 <br /> <br />|0x87D1B798 <br /> <br />|Internal error <br /> <br />|
|-2016300111 <br /> <br />|0x87D1B3B1 <br /> <br />|36001:(internal error) <br /> <br />|
|-2016300112 <br /> <br />|0x87D1B3B0 <br /> <br />|36000:Cellular already configured <br /> <br />|
|-2016301110 <br /> <br />|0x87D1AFCA <br /> <br />|35002:Multiple fonts in a single payload <br /> <br />|
|-2016301111 <br /> <br />|0x87D1AFC9 <br /> <br />|35001:Failed font installation <br /> <br />|
|-2016301112 <br /> <br />|0x87D1AFC8 <br /> <br />|35000:Invalid font data <br /> <br />|
|-2016302109 <br /> <br />|0x87D1ABE3 <br /> <br />|34003:Kerberos principal name invalid <br /> <br />|
|-2016302110 <br /> <br />|0x87D1ABE2 <br /> <br />|34002:Kerberos principal name missing <br /> <br />|
|-2016302111 <br /> <br />|0x87D1ABE1 <br /> <br />|34001:Invalid URL match pattern <br /> <br />|
|-2016302112 <br /> <br />|0x87D1ABE0 <br /> <br />|34000:Invalid app identifier match pattern <br /> <br />|
|-2016304112 <br /> <br />|0x87D1A410 <br /> <br />|32000:Too many apps <br /> <br />|
|-2016305111 <br /> <br />|0x87D1A029 <br /> <br />|31001:Cannot apply settings <br /> <br />|
|-2016305112 <br /> <br />|0x87D1A028 <br /> <br />|31000:Cannot apply credential <br /> <br />|
|-2016306111 <br /> <br />|0x87D19C41 <br /> <br />|30001:Timed out <br /> <br />|
|-2016306112 <br /> <br />|0x87D19C40 <br /> <br />|30000:Authentication failed <br /> <br />|
|-2016307109 <br /> <br />|0x87D1985B <br /> <br />|29003:Bad certificate data <br /> <br />|
|-2016307110 <br /> <br />|0x87D1985A <br /> <br />|29002: <br /> <br />|
|-2016307111 <br /> <br />|0x87D19859 <br /> <br />|29001: <br /> <br />|
|-2016307112 <br /> <br />|0x87D19858 <br /> <br />|29000:Device not supervised <br /> <br />|
|-2016308110 <br /> <br />|0x87D19472 <br /> <br />|28002:Cannot set wallpaper <br /> <br />|
|-2016308111 <br /> <br />|0x87D19471 <br /> <br />|28001:Bad wallpaper image <br /> <br />|
|-2016308112 <br /> <br />|0x87D19470 <br /> <br />|28000:Unknown item <br /> <br />|
|-2016310111 <br /> <br />|0x87D18CA1 <br /> <br />|26001:File level encryption unsupported <br /> <br />|
|-2016310112 <br /> <br />|0x87D18CA0 <br /> <br />|26000:Block level encryption unsupported <br /> <br />|
|-2016311110 <br /> <br />|0x87D188BA <br /> <br />|25002:Cannot remove <br /> <br />|
|-2016311111 <br /> <br />|0x87D188B9 <br /> <br />|25001:Cannot install <br /> <br />|
|-2016311112 <br /> <br />|0x87D188B8 <br /> <br />|25000:Bad profile <br /> <br />|
|-2016312109 <br /> <br />|0x87D184D3 <br /> <br />|24003:Bad final profile <br /> <br />|
|-2016312110 <br /> <br />|0x87D184D2 <br /> <br />|24002:Bad identity payload <br /> <br />|
|-2016312111 <br /> <br />|0x87D184D1 <br /> <br />|24001:Cannot sign attribute dictionary <br /> <br />|
|-2016312112 <br /> <br />|0x87D184D0 <br /> <br />|24000:Cannot create attribute dictionary <br /> <br />|
|-2016313110 <br /> <br />|0x87D180EA <br /> <br />|23002:Invalid server certificate <br /> <br />|
|-2016313111 <br /> <br />|0x87D180E9 <br /> <br />|23001:Bad server response <br /> <br />|
|-2016313112 <br /> <br />|0x87D180E8 <br /> <br />|23000:Bad identity <br /> <br />|
|-2016314099 <br /> <br />|0x87D17D0D <br /> <br />|22013:Invalid PKIOperation response <br /> <br />|
|-2016314100 <br /> <br />|0x87D17D0C <br /> <br />|22012:Cannot store CACertificate <br /> <br />|
|-2016314101 <br /> <br />|0x87D17D0B <br /> <br />|22011:Cannot generate CSR <br /> <br />|
|-2016314102 <br /> <br />|0x87D17D0A <br /> <br />|22010:Cannot store temporary identity <br /> <br />|
|-2016314103 <br /> <br />|0x87D17D09 <br /> <br />|22009:Cannot create temporary identity <br /> <br />|
|-2016314104 <br /> <br />|0x87D17D08 <br /> <br />|22008:Cannot create identity <br /> <br />|
|-2016314105 <br /> <br />|0x87D17D07 <br /> <br />|22007:Invalid signed certificate <br /> <br />|
|-2016314106 <br /> <br />|0x87D17D06 <br /> <br />|22006:Insufficient CACaps <br /> <br />|
|-2016314107 <br /> <br />|0x87D17D05 <br /> <br />|22005:Network error <br /> <br />|
|-2016314108 <br /> <br />|0x87D17D04 <br /> <br />|22004:Unsupported certificate configuration <br /> <br />|
|-2016314109 <br /> <br />|0x87D17D03 <br /> <br />|22003:Invalid RAResponse <br /> <br />|
|-2016314110 <br /> <br />|0x87D17D02 <br /> <br />|22002:Invalid CAResponse <br /> <br />|
|-2016314111 <br /> <br />|0x87D17D01 <br /> <br />|22001:Cannot generate key pair <br /> <br />|
|-2016314112 <br /> <br />|0x87D17D00 <br /> <br />|22000:Invalid key usage <br /> <br />|
|-2016315105 <br /> <br />|0x87D1791F <br /> <br />|21007:Cannot verify account <br /> <br />|
|-2016315106 <br /> <br />|0x87D1791E <br /> <br />|21006:Cannot decrypt certificate <br /> <br />|
|-2016315107 <br /> <br />|0x87D1791D <br /> <br />|21005:Account not unique <br /> <br />|
|-2016315108 <br /> <br />|0x87D1791C <br /> <br />|21004:Cannot create account <br /> <br />|
|-2016315109 <br /> <br />|0x87D1791B <br /> <br />|21003:No host name <br /> <br />|
|-2016315110 <br /> <br />|0x87D1791A <br /> <br />|21002:Cannot comply with encryption policy from server <br /> <br />|
|-2016315111 <br /> <br />|0x87D17919 <br /> <br />|21001:Cannot comply with policy from server <br /> <br />|
|-2016315112 <br /> <br />|0x87D17918 <br /> <br />|21000:Cannot get policy from server <br /> <br />|
|-2016316110 <br /> <br />|0x87D17532 <br /> <br />|20002:Account not unique <br /> <br />|
|-2016316111 <br /> <br />|0x87D17531 <br /> <br />|20001:No host name <br /> <br />|
|-2016316112 <br /> <br />|0x87D17530 <br /> <br />|20000:Cannot create account <br /> <br />|
|-2016317110 <br /> <br />|0x87D1714A <br /> <br />|19002:Account not unique <br /> <br />|
|-2016317111 <br /> <br />|0x87D17149 <br /> <br />|19001:No host name <br /> <br />|
|-2016317112 <br /> <br />|0x87D17148 <br /> <br />|19000:Cannot create account <br /> <br />|
|-2016318110 <br /> <br />|0x87D16D62 <br /> <br />|18002:Invalid credentials <br /> <br />|
|-2016318111 <br /> <br />|0x87D16D61 <br /> <br />|18001:Host unreachable <br /> <br />|
|-2016318112 <br /> <br />|0x87D16D60 <br /> <br />|18000:Unknown error <br /> <br />|
|-2016319110 <br /> <br />|0x87D1697A <br /> <br />|17002:Account not unique <br /> <br />|
|-2016319111 <br /> <br />|0x87D16979 <br /> <br />|17001:No host name <br /> <br />|
|-2016319112 <br /> <br />|0x87D16978 <br /> <br />|17000:Cannot create account <br /> <br />|
|-2016320110 <br /> <br />|0x87D16592 <br /> <br />|16002:Account not unique <br /> <br />|
|-2016320111 <br /> <br />|0x87D16591 <br /> <br />|16001:No host name <br /> <br />|
|-2016320112 <br /> <br />|0x87D16590 <br /> <br />|16000:Cannot create subscription <br /> <br />|
|-2016321109 <br /> <br />|0x87D161AB <br /> <br />|15003:Invalid certificate <br /> <br />|
|-2016321110 <br /> <br />|0x87D161AA <br /> <br />|15002:Cannot lock network configuration <br /> <br />|
|-2016321111 <br /> <br />|0x87D161A9 <br /> <br />|15001:Cannot remove VPN <br /> <br />|
|-2016321112 <br /> <br />|0x87D161A8 <br /> <br />|15000:Cannot install VPN <br /> <br />|
|-2016322110 <br /> <br />|0x87D15DC2 <br /> <br />|14002:Cloud configuration already exists <br /> <br />|
|-2016322111 <br /> <br />|0x87D15DC1 <br /> <br />|14001:Device locked <br /> <br />|
|-2016322112 <br /> <br />|0x87D15DC0 <br /> <br />|14000:Invalid field <br /> <br />|
|-2016323107 <br /> <br />|0x87D159DD <br /> <br />|13005:Cannot set up proxy <br /> <br />|
|-2016323108 <br /> <br />|0x87D159DC <br /> <br />|13004:Cannot set up EAP <br /> <br />|
|-2016323109 <br /> <br />|0x87D159DB <br /> <br />|13003:Cannot create WiFi configuration <br /> <br />|
|-2016323110 <br /> <br />|0x87D159DA <br /> <br />|13002:Password required <br /> <br />|
|-2016323111 <br /> <br />|0x87D159D9 <br /> <br />|13001:Username required <br /> <br />|
|-2016323112 <br /> <br />|0x87D159D8 <br /> <br />|13000:Cannot install <br /> <br />|
|-2016324070 <br /> <br />|0x87D1561A <br /> <br />|12042:Unknown locale code <br /> <br />|
|-2016324071 <br /> <br />|0x87D15619 <br /> <br />|12041:Unknown language code <br /> <br />|
|-2016324072 <br /> <br />|0x87D15618 <br /> <br />|12040:iTunes store login required <br /> <br />|
|-2016324073 <br /> <br />|0x87D15617 <br /> <br />|12039:(unused) <br /> <br />|
|-2016324074 <br /> <br />|0x87D15616 <br /> <br />|12038:App not managed <br /> <br />|
|-2016324075 <br /> <br />|0x87D15615 <br /> <br />|12037:Invalid redemption code <br /> <br />|
|-2016324076 <br /> <br />|0x87D15614 <br /> <br />|12036:Cannot remove app in current state <br /> <br />|
|-2016324077 <br /> <br />|0x87D15613 <br /> <br />|12035:App cannot be purchased <br /> <br />|
|-2016324078 <br /> <br />|0x87D15612 <br /> <br />|12034:URL is not HTTPS <br /> <br />|
|-2016324079 <br /> <br />|0x87D15611 <br /> <br />|12033:Invalid manifest <br /> <br />|
|-2016324080 <br /> <br />|0x87D15610 <br /> <br />|12032:Too many apps in manifest <br /> <br />|
|-2016324081 <br /> <br />|0x87D1560F <br /> <br />|12031:App installation disabled <br /> <br />|
|-2016324082 <br /> <br />|0x87D1560E <br /> <br />|12030:Invalid URL <br /> <br />|
|-2016324083 <br /> <br />|0x87D1560D <br /> <br />|12029:App not managed <br /> <br />|
|-2016324084 <br /> <br />|0x87D1560C <br /> <br />|12028:Not waiting for redemption <br /> <br />|
|-2016324085 <br /> <br />|0x87D1560B <br /> <br />|12027:Not an app <br /> <br />|
|-2016324086 <br /> <br />|0x87D1560A <br /> <br />|12026:App already queued <br /> <br />|
|-2016324087 <br /> <br />|0x87D15609 <br /> <br />|12025:App already installed <br /> <br />|
|-2016324088 <br /> <br />|0x87D15608 <br /> <br />|12024:Could not validate app manifest <br /> <br />|
|-2016324089 <br /> <br />|0x87D15607 <br /> <br />|12023:Could not validate app iD <br /> <br />|
|-2016324090 <br /> <br />|0x87D15606 <br /> <br />|12022:Invalid topic <br /> <br />|
|-2016324091 <br /> <br />|0x87D15605 <br /> <br />|12021:Invalid request type <br /> <br />|
|-2016324092 <br /> <br />|0x87D15604 <br /> <br />|12020:Unauthorized by server <br /> <br />|
|-2016324093 <br /> <br />|0x87D15603 <br /> <br />|12019:Cannot copy escrow secret <br /> <br />|
|-2016324094 <br /> <br />|0x87D15602 <br /> <br />|12018:Cannot copy escrow keybag data <br /> <br />|
|-2016324095 <br /> <br />|0x87D15601 <br /> <br />|12017:Cannot create escrow keybag <br /> <br />|
|-2016324096 <br /> <br />|0x87D15600 <br /> <br />|12016:Missing identity <br /> <br />|
|-2016324097 <br /> <br />|0x87D155FF <br /> <br />|12015:Cannot get push token <br /> <br />|
|-2016324098 <br /> <br />|0x87D155FE <br /> <br />|12014:Provisioning profile not managed <br /> <br />|
|-2016324099 <br /> <br />|0x87D155FD <br /> <br />|12013:Profile not managed <br /> <br />|
|-2016324100 <br /> <br />|0x87D155FC <br /> <br />|12012:MDM replacement mismatch <br /> <br />|
|-2016324101 <br /> <br />|0x87D155FB <br /> <br />|12011:Invalid MDM configuration <br /> <br />|
|-2016324102 <br /> <br />|0x87D155FA <br /> <br />|12010:Internal inconsistency error <br /> <br />|
|-2016324103 <br /> <br />|0x87D155F9 <br /> <br />|12009:Invalid replacement profile <br /> <br />|
|-2016324104 <br /> <br />|0x87D155F8 <br /> <br />|12008:Malformed request <br /> <br />|
|-2016324105 <br /> <br />|0x87D155F7 <br /> <br />|12007:Not authorized <br /> <br />|
|-2016324106 <br /> <br />|0x87D155F6 <br /> <br />|12006:Redirect refused <br /> <br />|
|-2016324107 <br /> <br />|0x87D155F5 <br /> <br />|12005:Cannot find certificate <br /> <br />|
|-2016324108 <br /> <br />|0x87D155F4 <br /> <br />|12004:Invalid push certificate <br /> <br />|
|-2016324109 <br /> <br />|0x87D155F3 <br /> <br />|12003:Invalid challenge response <br /> <br />|
|-2016324110 <br /> <br />|0x87D155F2 <br /> <br />|12002:Cannot check in <br /> <br />|
|-2016324111 <br /> <br />|0x87D155F1 <br /> <br />|12001:Multiple MDM instances <br /> <br />|
|-2016324112 <br /> <br />|0x87D155F0 <br /> <br />|12000:Invalid access rights <br /> <br />|
|-2016325111 <br /> <br />|0x87D15209 <br /> <br />|11001:Custom APN already installed <br /> <br />|
|-2016325112 <br /> <br />|0x87D15208 <br /> <br />|11000:Cannot install APN <br /> <br />|
|-2016326111 <br /> <br />|0x87D14E21 <br /> <br />|10001:Invalid signer <br /> <br />|
|-2016326112 <br /> <br />|0x87D14E20 <br /> <br />|10000:Cannot install defaults <br /> <br />|
|-2016327106 <br /> <br />|0x87D14A3E <br /> <br />|9006:Certificate is not an identity <br /> <br />|
|-2016327107 <br /> <br />|0x87D14A3D <br /> <br />|9005:Certificate is malformed <br /> <br />|
|-2016327108 <br /> <br />|0x87D14A3C <br /> <br />|9004:Cannot store root certificate <br /> <br />|
|-2016327109 <br /> <br />|0x87D14A3B <br /> <br />|9003:Cannot store WAPI data <br /> <br />|
|-2016327110 <br /> <br />|0x87D14A3A <br /> <br />|9002:Cannot store certificate <br /> <br />|
|-2016327111 <br /> <br />|0x87D14A39 <br /> <br />|9001:Too many certificates in a payload <br /> <br />|
|-2016327112 <br /> <br />|0x87D14A38 <br /> <br />|9000:Invalid password <br /> <br />|
|-2016328112 <br /> <br />|0x87D14650 <br /> <br />|8000:Cannot install Web Clip <br /> <br />|
|-2016329105 <br /> <br />|0x87D1426F <br /> <br />|7007:SMTP account is misconfigured <br /> <br />|
|-2016329106 <br /> <br />|0x87D1426E <br /> <br />|7006:POP account is misconfigured <br /> <br />|
|-2016329107 <br /> <br />|0x87D1426D <br /> <br />|7005:IMAP account is misconfigured <br /> <br />|
|-2016329108 <br /> <br />|0x87D1426C <br /> <br />|7004:SMIME certificate is bad <br /> <br />|
|-2016329109 <br /> <br />|0x87D1426B <br /> <br />|7003:SMIME certificate not found <br /> <br />|
|-2016329110 <br /> <br />|0x87D1426A <br /> <br />|7002:Unknown error occurred during validation <br /> <br />|
|-2016329111 <br /> <br />|0x87D14269 <br /> <br />|7001:Invalid credentials <br /> <br />|
|-2016329112 <br /> <br />|0x87D14268 <br /> <br />|7000:Host unreachable <br /> <br />|
|-2016330110 <br /> <br />|0x87D13E82 <br /> <br />|6002:Cannot create query <br /> <br />|
|-2016330111 <br /> <br />|0x87D13E81 <br /> <br />|6001:Empty string <br /> <br />|
|-2016330112 <br /> <br />|0x87D13E80 <br /> <br />|6000:Keychain system error <br /> <br />|
|-2016331097 <br /> <br />|0x87D13AA7 <br /> <br />|5015:Cannot set grace period <br /> <br />|
|-2016331098 <br /> <br />|0x87D13AA6 <br /> <br />|5014:Cannot set passcode <br /> <br />|
|-2016331099 <br /> <br />|0x87D13AA5 <br /> <br />|5013:Cannot clear passcode <br /> <br />|
|-2016331100 <br /> <br />|0x87D13AA4 <br /> <br />|5012:(unused) <br /> <br />|
|-2016331101 <br /> <br />| <br /> <br />|5011:Wrong passcode <br /> <br />|
|-2016331102 <br /> <br />| <br /> <br />|5010:Device locked <br /> <br />|
|-2016331103 <br /> <br />|0x87D13AA4 <br /> <br />|5009:(unused) <br /> <br />|
|-2016331104 <br /> <br />|0x87D13AA0 <br /> <br />|5008:Passcode too recent <br /> <br />|
|-2016331105 <br /> <br />|0x87D13A9F <br /> <br />|5007:Passcode expired <br /> <br />|
|-2016331106 <br /> <br />|0x87D13AA3 <br /> <br />|5006:Passcode requires alpha characters <br /> <br />|
|-2016331107 <br /> <br />|0x87D13A9D <br /> <br />|5005:Passcode requires number <br /> <br />|
|-2016331108 <br /> <br />|0x87D13A9C <br /> <br />|5004:Passcode has ascending descending characters <br /> <br />|
|-2016331109 <br /> <br />|0x87D13A9B <br /> <br />|5003:Passcode has repeating characters <br /> <br />|
|-2016331110 <br /> <br />|0x87D13A9A <br /> <br />|5002:Too few complex characters <br /> <br />|
|-2016331111 <br /> <br />|0x87D13A99 <br /> <br />|5001:Too few unique characters <br /> <br />|
|-2016331112 <br /> <br />|0x87D13A98 <br /> <br />|5000:Passcode too short <br /> <br />|
|-2016332093 <br /> <br />|0x87D136C3 <br /> <br />|4019:Multiple App Lock payloads <br /> <br />|
|-2016332094 <br /> <br />|0x87D136C2 <br /> <br />|4018:Multiple APN or Cellular payloads <br /> <br />|
|-2016332095 <br /> <br />|0x87D136C1 <br /> <br />|4017:Multiple global HTTPProxy payloads <br /> <br />|
|-2016332096 <br /> <br />|0x87D136C0 <br /> <br />|4016:(Internal error) <br /> <br />|
|-2016332097 <br /> <br />|0x87D136BF <br /> <br />|4015:Replacement profile does not contain an MDM payload <br /> <br />|
|-2016332098 <br /> <br />|0x87D136BE <br /> <br />|4014:No device identity available <br /> <br />|
|-2016332099 <br /> <br />|0x87D136BD <br /> <br />|4013:Update failed <br /> <br />|
|-2016332100 <br /> <br />|0x87D136BC <br /> <br />|4012:Profile is not updatable <br /> <br />|
|-2016332101 <br /> <br />|0x87D136BB <br /> <br />|4011:Final profile is not a configuration profile <br /> <br />|
|-2016332102 <br /> <br />|0x87D136BA <br /> <br />|4010:Updated profile does not have the same identifier <br /> <br />|
|-2016332103 <br /> <br />|0x87D136B9 <br /> <br />|4009:Device locked <br /> <br />|
|-2016332104 <br /> <br />|0x87D136B8 <br /> <br />|4008:Mismatched certificates <br /> <br />|
|-2016332105 <br /> <br />|0x87D136B7 <br /> <br />|4007:Unrecognized file format <br /> <br />|
|-2016332106 <br /> <br />|0x87D136B6 <br /> <br />|4006:Profile removal date is in the past <br /> <br />|
|-2016332107 <br /> <br />|0x87D136B5 <br /> <br />|4005:Passcode does not comply <br /> <br />|
|-2016332108 <br /> <br />|0x87D136B4 <br /> <br />|4004:User cancelled installation <br /> <br />|
|-2016332109 <br /> <br />|0x87D136B3 <br /> <br />|4003:Profile not queued for installation <br /> <br />|
|-2016332110 <br /> <br />|0x87D136B2 <br /> <br />|4002:Duplicate UUID <br /> <br />|
|-2016332111 <br /> <br />|0x87D136B1 <br /> <br />|4001:Installation failure <br /> <br />|
|-2016332112 <br /> <br />|0x87D136B0 <br /> <br />|4000:Cannot parse profile <br /> <br />|
|-2016333111 <br /> <br />|0x87D132C9 <br /> <br />|3001:Inconsistent value comparison sense (internal error) <br /> <br />|
|-2016333112 <br /> <br />|0x87D132C8 <br /> <br />|3000:Inconsistent restriction sense (internal error) <br /> <br />|
|-2016334108 <br /> <br />|0x87D12EE4 <br /> <br />|2004:Unsupported field value <br /> <br />|
|-2016334109 <br /> <br />|0x87D12EE3 <br /> <br />|2003:Bad data type in field <br /> <br />|
|-2016334110 <br /> <br />|0x87D12EE2 <br /> <br />|2002:Missing required field <br /> <br />|
|-2016334111 <br /> <br />|0x87D12EE1 <br /> <br />|2001:Unsupported payload version <br /> <br />|
|-2016334112 <br /> <br />|0x87D12EE0 <br /> <br />|2000:Malformed Payload <br /> <br />|
|-2016335102 <br /> <br />|0x87D12B02 <br /> <br />|1010:Unsupported field value <br /> <br />|
|-2016335103 <br /> <br />|0x87D12B01 <br /> <br />|1009:Profile installation failure <br /> <br />|
|-2016335104 <br /> <br />|0x87D12B00 <br /> <br />|1008:Non-unique payload identifiers <br /> <br />|
|-2016335105 <br /> <br />|0x87D12AFF <br /> <br />|1007:Non-unique UUIDs <br /> <br />|
|-2016335106 <br /> <br />|0x87D12AFE <br /> <br />|1006:Cannot decrypt <br /> <br />|
|-2016335107 <br /> <br />|0x87D12AFD <br /> <br />|1005:Empty profile <br /> <br />|
|-2016335108 <br /> <br />|0x87D12AFC <br /> <br />|1004:Bad signature <br /> <br />|
|-2016335109 <br /> <br />|0x87D12AFB <br /> <br />|1003:Bad data type in field <br /> <br />|
|-2016335110 <br /> <br />|0x87D12AFA <br /> <br />|1002:Missing required field <br /> <br />|
|-2016335111 <br /> <br />|0x87D12AF9 <br /> <br />|1001:Unsupported profile version <br /> <br />|
|-2016335112 <br /> <br />|0x87D12AF8 <br /> <br />|1000:Malformed profile <br /> <br />|

### OMA response codes

|Status code <br /> <br />|Hexadecimal error code <br /> <br />|Error message <br /> <br />|
|---------------|--------------------------|-----------------|
|-2016344008 <br /> <br />|0x87D10838 <br /> <br />|(1404): Certificate access denied <br /> <br />|
|-2016344009 <br /> <br />|0x87D10837 <br /> <br />|(1403): Certificate not found <br /> <br />|
|-2016344010 <br /> <br />|0x87D10836 <br /> <br />|DCMO(1402): The Operation failed <br /> <br />|
|-2016344011 <br /> <br />|0x87D10835 <br /> <br />|DCMO(1401): User chose not to accept the operation when prompted <br /> <br />|
|-2016344012 <br /> <br />|0x87D10834 <br /> <br />|DCMO(1400): Client error <br /> <br />|
|-2016344108 <br /> <br />|0x87D107D4 <br /> <br />|DCMO(1204): Device Capability is disabled and User is allowed to re-enable it <br /> <br />|
|-2016344109 <br /> <br />|0x87D107D3 <br /> <br />|DCMO(1203): Device Capability is disabled and User is not allowed to re-enable it <br /> <br />|
|-2016344110 <br /> <br />|0x87D107D2 <br /> <br />|DCMO(1202): Enable operation is performed successfully but the Device Capability is currently detached <br /> <br />|
|-2016344111 <br /> <br />|0xF3FB4D95 <br /> <br />|DCMO(1201): Enable operation is performed successfully and the Device Capability is currently attached <br /> <br />|
|-2016344112 <br /> <br />|0x87D107D0 <br /> <br />|DCMO(1200): Operation is performed successfully <br /> <br />|
|-2016345595 <br /> <br />|0x87D10205 <br /> <br />|Syncml(517): The response to an atomic command was too large to fit in a single message. <br /> <br />|
|-2016345596 <br /> <br />|0x87D10204 <br /> <br />|Syncml(516): Command was inside Atomic element and Atomic failed. This command was not rolled back successfully. <br /> <br />|
|-2016345598 <br /> <br />|0x87D10202 <br /> <br />|Syncml(514): The SyncML command was not completed successfully, since the operation was already cancelled before processing the command. <br /> <br />|
|-2016345599 <br /> <br />|0x87D10201 <br /> <br />|Syncml(513): The recipient does not support or refuses to support the specified version of the SyncML Synchronization Protocol used in the request SyncML Message. <br /> <br />|
|-2016345600 <br /> <br />|0x87D10200 <br /> <br />|Syncml(512): An application error occurred during the synchronization session. <br /> <br />|
|-2016345601 <br /> <br />|0x87D101FF <br /> <br />|Syncml(511): A severe error occurred in the server while processing the request. <br /> <br />|
|-2016345602 <br /> <br />|0x87D101FE <br /> <br />|Syncml(510): An error occurred while processing the request. The error is related to a failure in the recipient data store. <br /> <br />|
|-2016345603 <br /> <br />|0x87D101FD <br /> <br />|Syncml(509): Reserved for future use. <br /> <br />|
|-2016345604 <br /> <br />|0x87D101FC <br /> <br />|Syncml(508): An error occurred that necessitates a refresh of the current synchronization state of the client with the server. <br /> <br />|
|-2016345605 <br /> <br />|0x87D101FB <br /> <br />|Syncml(507): The error caused all SyncML commands within an Atomic element type to fail. <br /> <br />|
|-2016345606 <br /> <br />|0x87D101FA <br /> <br />|Syncml(506): An application error occurred while processing the request. <br /> <br />|
|-2016345607 <br /> <br />|0x87D101F9 <br /> <br />|Syncml(505): The recipient does not support or refuses to support the specified version of SyncML DTD used in the request SyncML Message. <br /> <br />|
|-2016345608 <br /> <br />|=0x87D101F8 <br /> <br />|Syncml(504): The recipient, while acting as a gateway or proxy, did not receive a timely response from the upstream recipient specified by the URI (e.g. HTTP, FTP, LDAP) or some other auxiliary recipient (e.g. DNS) it needed to access in attempting to complete the request. <br /> <br />|
|-2016345609 <br /> <br />|0x87D101F7 <br /> <br />|Syncml(503): The recipient is currently unable to handle the request due to a temporary overloading or maintenance of the recipient. <br /> <br />|
|-2016345610 <br /> <br />|0x87D101F6 <br /> <br />|Syncml(502): The recipient, while acting as a gateway or proxy, received an invalid response from the upstream recipient it accessed in attempting to fulfill the request. <br /> <br />|
|-2016345611 <br /> <br />|0x87D101F5 <br /> <br />|Syncml(501): The recipient does not support the command required to fulfill the request. <br /> <br />|
|-2016345612 <br /> <br />|0x87D101F4 <br /> <br />|Syncml(500): The recipient encountered an unexpected condition which prevented it from fulfilling the request <br /> <br />|
|-2016345684 <br /> <br />|0x87D101AC <br /> <br />|Syncml(428): Move failed <br /> <br />|
|-2016345685 <br /> <br />|0x87D101AB <br /> <br />|Syncml(427): Parent cannot be deleted since it contains children. <br /> <br />|
|-2016345686 <br /> <br />|0x87D101AA <br /> <br />|Syncml(426): Partial item not accepted. <br /> <br />|
|-2016345687 <br /> <br />|0x87D101A9 <br /> <br />|Syncml(425): The requested command failed because the sender does not have adequate access control permissions (ACL) on the recipient. <br /> <br />|
|-2016345688 <br /> <br />|0x87D101A8 <br /> <br />|Syncml(424): The chunked object was received, but the size of the received object did not match the size declared within the first chunk. <br /> <br />|
|-2016345689 <br /> <br />|0x87D101A7 <br /> <br />|Syncml(423): The requested command failed because the "Soft Deleted" item was previously "Hard Deleted" on the server. <br /> <br />|
|-2016345690 <br /> <br />|0x87D101A6 <br /> <br />|Syncml(422): The requested command failed on the server because the CGI scripting in the LocURI was incorrectly formed. <br /> <br />|
|-2016345691 <br /> <br />|0x87D101A5 <br /> <br />|Syncml(421): The requested command failed on the server because the specified search grammar was not known. <br /> <br />|
|-2016345692 <br /> <br />|0x87D101A4 <br /> <br />|Syncml(420): The recipient has no more storage space for the remaining synchronization data. <br /> <br />|
|-2016345693 <br /> <br />|0x87D101A3 <br /> <br />|Syncml(419): The client request created a conflict which was resolved by the server command winning. <br /> <br />|
|-2016345694 <br /> <br />|0x87D101A2 <br /> <br />|Syncml(418): The requested Put or Add command failed because the target already exists. <br /> <br />|
|-2016345695 <br /> <br />|0x87D101A1 <br /> <br />|Syncml(417): The request failed at this time and the originator should retry the request later. <br /> <br />|
|-2016345696 <br /> <br />|0x87D101A0 <br /> <br />|Syncml(416): The request failed because the specified byte size in the request was too big. <br /> <br />|
|-2016345697 <br /> <br />|0x87D1019F <br /> <br />|Syncml(415): Unsupported media type or format. <br /> <br />|
|-2016345698 <br /> <br />|0x87D1019E <br /> <br />|Syncml(414): The requested command failed because the target URI is too long for what the recipient is able or willing to process. <br /> <br />|
|-2016345699 <br /> <br />|0x87D1019D <br /> <br />|Syncml(413): The recipient is refusing to perform the requested command because the requested item is larger than the recipient is able or willing to process. <br /> <br />|
|-2016345700 <br /> <br />|0x87D1019C <br /> <br />|Syncml(412): The requested command failed on the recipient because it was incomplete or incorrectly formed. <br /> <br />|
|-2016345701 <br /> <br />|0x87D1019B <br /> <br />|Syncml(411): The requested command must be accompanied by byte size or length information in the Meta element type. <br /> <br />|
|-2016345702 <br /> <br />|0x87D1019A <br /> <br />|Syncml(410): The requested target is no longer on the recipient and no forwarding URI is known. <br /> <br />|
|-2016345703 <br /> <br />|0x87D10199 <br /> <br />|Syncml(409): The requested failed because of an update conflict between the client and server versions of the data. <br /> <br />|
|-2016345704 <br /> <br />|0x87D10198 <br /> <br />|Syncml(408): An expected message was not received within the required period of time. <br /> <br />|
|-2016345705 <br /> <br />|0x87D10197 <br /> <br />|Syncml(407): The requested command failed because the originator must provide proper authentication. <br /> <br />|
|-2016345706 <br /> <br />|0x87D10196 <br /> <br />|Syncml(406): The requested command failed because an optional feature in the request was not supported. <br /> <br />|
|-2016345707 <br /> <br />|0x87D10195 <br /> <br />|Syncml(405): The requested command is not allowed on the target. <br /> <br />|
|-2016345708 <br /> <br />|0x87D10194 <br /> <br />|Syncml(404): The requested target was not found. <br /> <br />|
|-2016345709 <br /> <br />|0x87D10193 <br /> <br />|Syncml(403): The requested command failed, but the recipient understood the requested command. <br /> <br />|
|-2016345710 <br /> <br />|0x87D10192 <br /> <br />|Syncml(402): The requested command failed because proper payment is needed. <br /> <br />|
|-2016345711 <br /> <br />|0x87D10191 <br /> <br />|Syncml(401): The requested command failed because the requestor must provide proper authentication. <br /> <br />|
|-2016345712 <br /> <br />|0x87D10190 <br /> <br />|Syncml(400): The requested command could not be performed because of malformed syntax in the command. <br /> <br />|
|-2016345807 <br /> <br />|0x87D10131 <br /> <br />|Syncml(305): The requested target must be accessed through the specified proxy URI. <br /> <br />|
|-2016345808 <br /> <br />|0x87D10130 <br /> <br />|Syncml(304):The requested SyncML command was not executed on the target. <br /> <br />|
|-2016345809 <br /> <br />|0x87D1012F <br /> <br />|Syncml(303): The requested target can be found at another URI. <br /> <br />|
|-2016345810 <br /> <br />|0x87D1012E <br /> <br />|Syncml(302): The requested target has temporarily moved to a different URI. <br /> <br />|
|-2016345811 <br /> <br />|0x87D1012D <br /> <br />|Syncml(301): The requested target has a new URI. <br /> <br />|
|-2016345812 <br /> <br />|0x87D1012C <br /> <br />|Syncml(300): The requested target is one of a number of multiple alternatives requested target. <br /> <br />|
|-2016345896 <br /> <br />|0x87D100D8 <br /> <br />|Syncml(216): A command was inside Atomic element and Atomic failed. This command was rolled back successfully. <br /> <br />|
|-2016345897 <br /> <br />|0x87D100D7 <br /> <br />|Syncml(215): A command was not executed, as a result of user interaction and user chose not to accept the choice. <br /> <br />|
|-2016345898 <br /> <br />|0x87D100D6 <br /> <br />|Syncml(214): Operation cancelled. The SyncML command completed successfully, but no more commands will be processed within the session. <br /> <br />|
|-2016345899 <br /> <br />|0x87D100D5 <br /> <br />|Syncml(213): Chunked item accepted and buffered <br /> <br />|
|-2016345900 <br /> <br />|0x87D100D4 <br /> <br />|Syncml(212): Authentication accepted. No further authentication is needed for the remainder of the synchronization session. This response code can only be used in response to a request in which the credentials were provided. <br /> <br />|
|-2016345901 <br /> <br />|0x87D100D3 <br /> <br />|Syncml(211): Item not deleted. The requested item was not found. It could have been previously deleted. <br /> <br />|
|-2016345902 <br /> <br />|0x87D100D2 <br /> <br />|Syncml(210): Delete without archive. The response indicates that the requested data was successfully deleted, but that it was not archived prior to deletion because this OPTIONAL feature was not supported by the implementation. <br /> <br />|
|-2016345903 <br /> <br />|0x87D100D1 <br /> <br />|Conflict resolved with duplicate. The response indicates that the request created an update conflict; which was resolved with a duplication of the client's data being created in the server database. The response includes both the target URI of the duplicate in the Item of the Status. In addition, in the case of a two-way synchronization, an Add command is returned with the duplicate data definition. <br /> <br />|
|-2016345904 <br /> <br />|0x87D100D0 <br /> <br />|Conflict resolved with client's command "winning". The response indicates that there was an update conflict; which was resolved by the client command winning. <br /> <br />|
|-2016345905 <br /> <br />|0x87D100CF <br /> <br />|Conflict resolved with merge. The response indicates that the request created a conflict; which was resolved with a merge of the client and server instances of the data. The response includes both the Target and Source URLs in the Item of the Status. In addition, a Replace command is returned with the merged data. <br /> <br />|
|-2016345906 <br /> <br />|0x87D100CE <br /> <br />|The response indicates that only part of the command was completed. If the remainder of the command can be completed later, then when completed another appropriate completion request status code SHOULD be created. <br /> <br />|
|-2016345907 <br /> <br />|0x87D100CD <br /> <br />|The source SHOULD update their content. The originator of the request is being told that their content SHOULD be synchronized to get an up to date version. <br /> <br />|
|-2016345908 <br /> <br />|0x87D100CC <br /> <br />|The request was successfully completed but no data is being returned. The response code is also returned in response to a Get when the target has no content. <br /> <br />|
|-2016345909 <br /> <br />|0x87D100CB <br /> <br />|Non-authoritative response. The request is being responded to by an entity other than the one targeted. The response is only to be returned when the request would have been resulted in a 200 response code from the authoritative target. <br /> <br />|
|-2016345910 <br /> <br />|0x87D100CA <br /> <br />|Accepted for processing. The request to either run a remote execution of an application or to alert a user or application was successfully performed. <br /> <br />|
|-2016345911 <br /> <br />|0x87D100C9 <br /> <br />|The requested item was added. <br /> <br />|
|-2016345912 <br /> <br />|0x87D100C8 <br /> <br />|The SyncML command completed successfully. <br /> <br />|
|-2016346011 <br /> <br />|0x87D10065 <br /> <br />|The specified SyncML command is being carried out, but has not yet completed. <br /> <br />|

## See Also
[Enable access to company resources with Microsoft Intune](http://msdn.microsoft.com/en-us/library/5b090c5a-6f12-4e60-ace0-c9929afaa9a3)

