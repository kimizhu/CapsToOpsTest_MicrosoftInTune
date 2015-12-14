---
description: na
keywords: na
pagetitle: Troubleshoot software updates in Microsoft Intune
search: na
ms.author: 03258b9b-2cea-4654-ab05-a27214174f4b
ms.date: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d17b70f4-17b4-4d89-88fd-70fa4f34fbea
---
# Troubleshoot software updates in Microsoft Intune

## <a name="BKMK_Updates"></a>Troubleshooting software updates
Use the information in this section to help you solve software update problems in [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].

### Software update error codes
The following table lists the [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Update Agent error codes. If you cannot find a specific error code in this table, see [Windows Update Agent Result Codes](http://go.microsoft.com/fwlink/?LinkID=221542).

|Error code <br /> <br />|Symbolic name <br /> <br />|More information <br /> <br />|
|--------------|-----------------|--------------------|
|**0x00cf0001** <br /> <br />|OM_S_SERVICE_STOP <br /> <br />|The agent was successfully stopped. <br /> <br />|
|**0x00cf0003** <br /> <br />|OM_S_UPDATE_ERROR <br /> <br />|The operation was completed successfully, but errors occurred during the application of updates. <br /> <br />|
|**0x00cf0004** <br /> <br />|OM_S_MARKED_FOR_DISCONNECT <br /> <br />|A callback was marked to be disconnected later because the request to disconnect the operation occurred while a callback was running. <br /> <br />|
|**0x00cf0005** <br /> <br />|OM_S_REBOOT_REQUIRED <br /> <br />|The system must be restarted to complete the update installation. <br /> <br />|
|**0x00cf0006** <br /> <br />|OM_S_ALREADY_INSTALLED <br /> <br />|The update to be installed is already installed on the system. <br /> <br />|
|**0x00cf0007** <br /> <br />|OM_S_ALREADY_UNINSTALLED <br /> <br />|The update to be removed is not installed on the system. <br /> <br />|
|**0x00cf2015** <br /> <br />|OM_S_UH_INSTALLSTILLPENDING <br /> <br />|The update installation is in progress. <br /> <br />|
|**0x80cf0001** <br /> <br />|OM_E_NO_SERVICE <br /> <br />|The agent could not provide the service. <br /> <br />|
|**0x80cf0002** <br /> <br />|OM_E_MAX_CAPACITY_REACHED <br /> <br />|The maximum capacity of the service was exceeded. <br /> <br />|
|**0x80cf0003** <br /> <br />|OM_E_UNKNOWN_ID <br /> <br />|An ID cannot be found. <br /> <br />|
|**0x80cf0004** <br /> <br />|OM_E_NOT_INITIALIZED <br /> <br />|The object could not be initialized. <br /> <br />|
|**0x80cf0007** <br /> <br />|OM_E_INVALIDINDEX <br /> <br />|The index to a collection is not valid. <br /> <br />|
|**0x80cf0008** <br /> <br />|OM_E_ITEMNOTFOUND <br /> <br />|The key for the queried item could not be found. <br /> <br />|
|**0x80cf0009** <br /> <br />|OM_E_OPERATIONINPROGRESS <br /> <br />|A conflicting operation was in progress. Some operations, like multiple installations cannot be performed simultaneously. <br /> <br />|
|**0x80cf000B** <br /> <br />|OM_E_CALL_CANCELLED <br /> <br />|The operation was canceled. <br /> <br />|
|**0x80cf000C** <br /> <br />|OM_E_NOOP <br /> <br />|No operation was required. <br /> <br />|
|**0x80cf000D** <br /> <br />|OM_E_XML_MISSINGDATA <br /> <br />|The agent could not find required information in the update's XML data. <br /> <br />|
|**0x80cf000E** <br /> <br />|OM_E_XML_INVALID <br /> <br />|The agent found information in the update's XML data that is not valid. <br /> <br />|
|**0x80cf000F** <br /> <br />|OM_E_CYCLE_DETECTED <br /> <br />|Circular update relationships were detected in the metadata. <br /> <br />|
|**0x80cf0010** <br /> <br />|OM_E_TOO_DEEP_RELATION <br /> <br />|The update relationships were too deeply nested to evaluate. <br /> <br />|
|**0x80cf0011** <br /> <br />|OM_E_INVALID_RELATIONSHIP <br /> <br />|An update relationship was found that is not valid. <br /> <br />|
|**0x80cf0012** <br /> <br />|OM_E_REG_VALUE_INVALID <br /> <br />|A registry value was read that is not valid. <br /> <br />|
|**0x80cf0013** <br /> <br />|OM_E_DUPLICATE_ITEM <br /> <br />|The operation tried to add a duplicate item to a list. <br /> <br />|
|**0x80cf0014** <br /> <br />|OM_E_INVALID_INSTALL_REQUESTED <br /> <br />|The caller cannot install updates that were requested for installation. <br /> <br />|
|**0x80cf0016** <br /> <br />|OM_E_INSTALL_NOT_ALLOWED <br /> <br />|The operation tried to install while another installation was in progress, or the system was pending a mandatory restart. <br /> <br />|
|**0x80cf0017** <br /> <br />|OM_E_NOT_APPLICABLE <br /> <br />|The operation was not performed because there are no applicable updates. <br /> <br />|
|**0x80cf0018** <br /> <br />|OM_E_NO_USERTOKEN <br /> <br />|The operation failed because a required user token is missing. <br /> <br />|
|**0x80cf0019** <br /> <br />|OM_E_EXCLUSIVE_INSTALL_CONFLICT <br /> <br />|An exclusive update cannot be simultaneously installed together with other updates. <br /> <br />|
|**0x80cf001A** <br /> <br />|OM_E_POLICY_NOT_SET <br /> <br />|A policy value was not set. <br /> <br />|
|**0x80cf001D** <br /> <br />|OM_E_INVALID_UPDATE <br /> <br />|An update contains metadata that is not valid. <br /> <br />|
|**0x80cf001E** <br /> <br />|OM_E_SERVICE_STOP <br /> <br />|The operation could not be completed because the service or system was being shut down. <br /> <br />|
|**0x80cf001F** <br /> <br />|OM_E_NO_CONNECTION <br /> <br />|The operation could not be completed because the network connection was not available. <br /> <br />|
|**0x80cf0020** <br /> <br />|OM_E_NO_INTERACTIVE_USER <br /> <br />|The operation could not be completed because there is no logged-on interactive user. <br /> <br />|
|**0x80cf0021** <br /> <br />|OM_E_TIME_OUT <br /> <br />|The operation could not be completed because it timed out. <br /> <br />|
|**0x80cf0022** <br /> <br />|OM_E_ALL_UPDATES_FAILED <br /> <br />|The operation failed for all the updates. <br /> <br />|
|**0x80cf0024** <br /> <br />|OM_E_NO_UPDATE <br /> <br />|There are no updates. <br /> <br />|
|**0x80cf0025** <br /> <br />|OM_E_USER_ACCESS_DISABLED <br /> <br />|Group Policy settings prevented access to Windows Update. <br /> <br />|
|**0x80cf0026** <br /> <br />|OM_E_INVALID_UPDATE_TYPE <br /> <br />|The update type is not valid. <br /> <br />|
|**0x80cf0028** <br /> <br />|OM_E_UNINSTALL_NOT_ALLOWED <br /> <br />|The update could not be uninstalled because the request did not originate from a WSUS server. <br /> <br />|
|**0x80cf0029** <br /> <br />|OM_E_INVALID_PRODUCT_LICENSE <br /> <br />|Search might have missed some updates, or there might be an unlicensed application on the system. <br /> <br />|
|**0x80cf002C** <br /> <br />|OM_E_BIN_SOURCE_ABSENT <br /> <br />|A delta-compressed update could not be installed because it required the source. <br /> <br />|
|**0x80cf002D** <br /> <br />|OM_E_SOURCE_ABSENT <br /> <br />|A full-file update could not be installed because it required the source. <br /> <br />|
|**0x80cf002E** <br /> <br />|OM_E_WU_DISABLED <br /> <br />|Access to an unmanaged server is not allowed. <br /> <br />|
|**0x80cf002F** <br /> <br />|OM_E_CALL_CANCELLED_BY_POLICY <br /> <br />|The operation could not be completed because the **DisableWindowsUpdateAccess** policy was set. <br /> <br />|
|**0x80cf0030** <br /> <br />|OM_E_INVALID_PROXY_SERVER <br /> <br />|The proxy list format is not valid. <br /> <br />|
|**0x80cf0031** <br /> <br />|OM_E_INVALID_FILE <br /> <br />|The file is in the wrong format. <br /> <br />|
|**0x80cf0032** <br /> <br />|OM_E_INVALID_CRITERIA <br /> <br />|The search criteria string is not valid. <br /> <br />|
|**0x80cf0034** <br /> <br />|OM_E_DOWNLOAD_FAILED <br /> <br />|The update failed to download. <br /> <br />|
|**0x80cf0035** <br /> <br />|OM_E_UPDATE_NOT_PROCESSED <br /> <br />|The update was not processed. <br /> <br />|
|**0x80cf0036** <br /> <br />|OM_E_INVALID_OPERATION <br /> <br />|The object's current state did not allow the operation. <br /> <br />|
|**0x80cf0037** <br /> <br />|OM_E_NOT_SUPPORTED <br /> <br />|The operation is not supported. <br /> <br />|
|**0x80cf0038** <br /> <br />|OM_E_WINHTTP_INVALID_FILE <br /> <br />|The downloaded file has an unexpected content type. <br /> <br />|
|**0x80cf0039** <br /> <br />|OM_E_TOO_MANY_RESYNC <br /> <br />|The server asked the agent to resync too many times. <br /> <br />|
|**0x80cf0043** <br /> <br />|OM_E_NO_UI_SUPPORT <br /> <br />|There is no support for WUA UI. <br /> <br />|
|**0x80cf0044** <br /> <br />|OM_E_PER_MACHINE_UPDATE_ACCESS_DENIED <br /> <br />|Only administrators can perform this operation on per-computer updates. <br /> <br />|
|**0x80cf0045** <br /> <br />|OM_E_UNSUPPORTED_SEARCHSCOPE <br /> <br />|A search was attempted with an unsupported scope. <br /> <br />|
|**0x80cf0046** <br /> <br />|OM_E_BAD_FILE_URL <br /> <br />|The URL does not point to a file. <br /> <br />|
|**0x80cf0047** <br /> <br />|OM_E_NOTSUPPORTED <br /> <br />|The requested operation is not supported. <br /> <br />|
|**0x80cf0049** <br /> <br />|OM_E_OUTOFRANGE <br /> <br />|The data is out of range. <br /> <br />|
|**0x80cf004A** <br /> <br />|OM_E_INVALIDWUAVERSION <br /> <br />|The data contains a version that is not valid. <br /> <br />|
|**0x80cf004B** <br /> <br />|OM_E_SEARCH_COMPLETED_WITH_SOME_FAILURES <br /> <br />|The search call was completed, but failed to detect some of the updates. <br /> <br />|
|**0x80cf004C** <br /> <br />|OM_E_DOWNLOAD_COMPLETED_WITH_SOME_FAILURES <br /> <br />|The download call was completed, but failed to download some of the updates. <br /> <br />|
|**0x80cf004D** <br /> <br />|OM_E_INSTALL_COMPLETED_WITH_SOME_FAILURES <br /> <br />|The install call was completed, but failed to install some of the updates. <br /> <br />|
|**0x80cf004E** <br /> <br />|OM_E_WINUPDATE_CACHE_UNINITIALIZED <br /> <br />|The Windows Update cache is empty because it has not been initialized. <br /> <br />|
|**0x80cf0436** <br /> <br />|OM_E_PT_CATALOG_SYNC_REQUIRED <br /> <br />|The server does not support category-specific search. Full catalog search must be issued instead. <br /> <br />|
|**0x80cf0437** <br /> <br />|OM_E_PT_SECURITY_VERIFICATION_FAILURE <br /> <br />|There was a problem authorizing with the service. <br /> <br />|
|**0x80cf0438** <br /> <br />|OM_E_PT_ENDPOINT_UNREACHABLE <br /> <br />|There is no route or network connectivity to the endpoint. <br /> <br />|
|**0x80cf0439** <br /> <br />|OM_E_PT_INVALID_FORMAT <br /> <br />|The data received does not meet the data contract expectations. <br /> <br />|
|**0x80cf043A** <br /> <br />|OM_E_PT_INVALID_URL <br /> <br />|The URL is not valid. <br /> <br />|
|**0x80cf043B** <br /> <br />|OM_E_PT_NWS_NOT_LOADED <br /> <br />|The NWS runtime cannot be loaded. <br /> <br />|
|**0x80cf043C** <br /> <br />|OM_E_PT_PROXY_AUTH_SCHEME_NOT_SUPPORTED <br /> <br />|The proxy authentication scheme is not supported. <br /> <br />|
|**0x80cf043D** <br /> <br />|OM_E_SERVICEPROP_NOTAVAIL <br /> <br />|The requested service property is not available. <br /> <br />|
|**0x80cf043E** <br /> <br />|OM_E_PT_ENDPOINT_REFRESH_REQUIRED <br /> <br />|The endpoint provider plug-in requires an online refresh. <br /> <br />|
|**0x80cf043F** <br /> <br />|OM_E_PT_ENDPOINTURL_NOTAVAIL <br /> <br />|A URL for the requested service endpoint is not available. <br /> <br />|
|**0x80cf0440** <br /> <br />|OM_E_PT_ENDPOINT_DISCONNECTED <br /> <br />|The connection to the service endpoint terminated. <br /> <br />|
|**0x80cf0441** <br /> <br />|OM_E_PT_INVALID_OPERATION <br /> <br />|The operation is not valid because protocol talker is in an inappropriate state. <br /> <br />|
|**0x80cf0FFF** <br /> <br />|OM_E_UNEXPECTED <br /> <br />|An operation failed because of reasons that are not explained by another error code. <br /> <br />|
|**0x80cf1001** <br /> <br />|OM_E_MSI_WRONG_VERSION <br /> <br />|Search might have missed some updates because the Windows Installer is an earlier version than version 3.1. <br /> <br />|
|**0x80cf1002** <br /> <br />|OM_E_MSI_NOT_CONFIGURED <br /> <br />|Search might have missed some updates because the Windows Installer is not configured. <br /> <br />|
|**0x80cf1003** <br /> <br />|OM_E_MSP_DISABLED <br /> <br />|Search might have missed some updates because policy has disabled Windows Installer patching. <br /> <br />|
|**0x80cf1004** <br /> <br />|OM_E_MSI_WRONG_APP_CONTEXT <br /> <br />|An update could not be applied because the application is installed per user. <br /> <br />|
|**0x80cf2000** <br /> <br />|OM_E_UH_REMOTEUNAVAILABLE <br /> <br />|A request for a remote update handler could not be completed because no remote process is available. <br /> <br />|
|**0x80cf2001** <br /> <br />|OM_E_UH_LOCALONLY <br /> <br />|A request for a remote update handler could not be completed because the handler is local only. <br /> <br />|
|**0x80cf2003** <br /> <br />|OM_E_UH_REMOTEALREADYACTIVE <br /> <br />|A remote update handler could not be created because one already exists. <br /> <br />|
|**0x80cf2004** <br /> <br />|OM_E_UH_DOESNOTSUPPORTACTION <br /> <br />|A request for the handler to install (uninstall) an update could not be completed because the update does not support install (uninstall). <br /> <br />|
|**0x80cf2005** <br /> <br />|OM_E_UH_WRONGHANDLER <br /> <br />|An operation could not be completed because the wrong handler was specified. <br /> <br />|
|**0x80cf2006** <br /> <br />|OM_E_UH_INVALIDMETADATA <br /> <br />|A handler operation could not be completed because the update contains metadata that is not valid. <br /> <br />|
|**0x80cf2007** <br /> <br />|OM_E_UH_INSTALLERHUNG <br /> <br />|An operation could not be completed because the installer exceeded the time limit. Check whether an update that requires user interaction was approved for deployment. In this case, you must revise the update installation parameters so that it can install silently. <br /> <br />|
|**0x80cf2008** <br /> <br />|OM_E_UH_OPERATIONCANCELLED <br /> <br />|An operation that was being performed by the update handler was canceled. <br /> <br />|
|**0x80cf2009** <br /> <br />|OM_E_UH_BADHANDLERXML <br /> <br />|An operation could not be completed because the handler-specific metadata is not valid. <br /> <br />|
|**0x80cf200B** <br /> <br />|OM_E_UH_INSTALLERFAILURE <br /> <br />|The installer failed to install (uninstall) one or more updates. <br /> <br />|
|**0x80cf200D** <br /> <br />|OM_E_UH_NEEDANOTHERDOWNLOAD <br /> <br />|The update handler did not install the update because it must be downloaded again. <br /> <br />|
|**0x80cf200E** <br /> <br />|OM_E_UH_NOTIFYFAILURE <br /> <br />|The update handler failed to send notification of the status of the install (uninstall) operation. <br /> <br />|
|**0x80cf2014** <br /> <br />|OM_E_UH_POSTREBOOTSTILLPENDING <br /> <br />|The post-reboot operation for the update is still in progress. <br /> <br />|
|**0x80cf2015** <br /> <br />|OM_E_UH_POSTREBOOTRESULTUNKNOWN <br /> <br />|The result of the post-reboot operation for the update could not be determined. <br /> <br />|
|**0x80cf2016** <br /> <br />|OM_E_UH_POSTREBOOTUNEXPECTEDSTATE <br /> <br />|The state of the update after its post-reboot operation was completed is unexpected. <br /> <br />|
|**0x80cf2017** <br /> <br />|OM_E_UH_NEW_SERVICING_STACK_REQUIRED <br /> <br />|The operation system servicing stack must be updated before this update is downloaded or installed. <br /> <br />|
|**0x80cf2018** <br /> <br />|OM_E_UH_CALLED_BACK_FAILURE <br /> <br />|A callback installer called back with an error. <br /> <br />|
|**0x80cf2019** <br /> <br />|OM_E_UH_CUSTOMINSTALLER_INVALID_SIGNATURE <br /> <br />|The custom installer signature did not match the signature that the update requires. <br /> <br />|
|**0x80cf201A** <br /> <br />|OM_E_UH_UNSUPPORTED_INSTALLCONTEXT <br /> <br />|The installer does not support the installation configuration. <br /> <br />|
|**0x80cf201B** <br /> <br />|OM_E_UH_INVALID_TARGETSESSION <br /> <br />|The targeted session for the installation is not valid. <br /> <br />|
|**0x80cf2FFF** <br /> <br />|OM_E_UH_UNEXPECTED <br /> <br />|An update handler error is not covered by another OM_E_UH_&#42; code. <br /> <br />|
|**0x80cf3FFD** <br /> <br />|OM_E_NON_UI_MODE <br /> <br />|Cannot show UI when in non-UI mode. Windows Update client UI modules might not be installed. <br /> <br />|
|**0x80cf3FFE** <br /> <br />|OM_E_WUCLTUI_UNSUPPORTED_VERSION <br /> <br />|This version of WU client UI exported functions is not supported. <br /> <br />|
|**0x80cf3FFF** <br /> <br />|OM_E_AUCLIENT_UNEXPECTED <br /> <br />|A user interface error occurred that is not covered by another OM_E_AUCLIENT_&#42; error code. <br /> <br />|
|**0x80cf4007** <br /> <br />|OM_E_PT_SOAPCLIENT_SOAPFAULT <br /> <br />|Same as **SOAPCLIENT_SOAPFAULT**. SOAP client failed because a SOAP fault of **OM_E_PT_SOAP_&#42;** error code type occurred. <br /> <br />|
|**0x80cf4008** <br /> <br />|OM_E_PT_SOAPCLIENT_PARSEFAULT <br /> <br />|Same as **SOAPCLIENT_PARSEFAULT_ERROR**.  SOAP client failed to parse a SOAP fault error. <br /> <br />|
|**0x80cf400A** <br /> <br />|OM_E_PT_SOAPCLIENT_PARSE <br /> <br />|Same as **SOAPCLIENT_PARSE_ERROR**.  SOAP client failed to parse the response from the server. <br /> <br />|
|**0x80cf400B** <br /> <br />|OM_E_PT_SOAP_VERSION <br /> <br />|Same as **SOAP_E_VERSION_MISMATCH**. SOAP client found an unrecognizable namespace for the SOAP envelope. <br /> <br />|
|**0x80cf400C** <br /> <br />|OM_E_PT_SOAP_MUST_UNDERSTAND <br /> <br />|Same as **SOAP_E_MUST_UNDERSTAND**. SOAP client could not interpret a header. <br /> <br />|
|**0x80cf400D** <br /> <br />|OM_E_PT_SOAP_CLIENT <br /> <br />|Same as **SOAP_E_CLIENT**. SOAP client found the message was malformed. Correct before resending. <br /> <br />|
|**0x80cf400E** <br /> <br />|OM_E_PT_SOAP_SERVER <br /> <br />|Same as **SOAP_E_SERVER**. The SOAP message could not be processed because of a server error. Resend later. <br /> <br />|
|**0x80cf4010** <br /> <br />|OM_E_PT_EXCEEDED_MAX_SERVER_TRIPS <br /> <br />|The number of round trips to the server exceeded the maximum limit. <br /> <br />|
|**0x80cf4012** <br /> <br />|OM_E_PT_DOUBLE_INITIALIZATION <br /> <br />|The initialization failed because the object was already initialized. <br /> <br />|
|**0x80cf4013** <br /> <br />|OM_E_PT_INVALID_COMPUTER_NAME <br /> <br />|The computer name could not be determined. <br /> <br />|
|**0x80cf4015** <br /> <br />|OM_E_PT_REFRESH_CACHE_REQUIRED <br /> <br />|The reply from the server indicates that the server was changed or the cookie was invalid. Refresh the internal cache and retry. <br /> <br />|
|**0x80cf4016** <br /> <br />|OM_E_PT_HTTP_STATUS_BAD_REQUEST <br /> <br />|Same as **HTTP status 400**. The server could not process the request because the syntax is not valid. <br /> <br />|
|**0x80cf4017** <br /> <br />|OM_E_PT_HTTP_STATUS_DENIED <br /> <br />|Same as **HTTP status 401**. The requested resource requires user authentication. <br /> <br />|
|**0x80cf4018** <br /> <br />|OM_E_PT_HTTP_STATUS_FORBIDDEN <br /> <br />|Same as **HTTP status 403**. The server understood the request, but declined to fulfill it. <br /> <br />|
|**0x80cf4019** <br /> <br />|OM_E_PT_HTTP_STATUS_NOT_FOUND <br /> <br />|Same as **HTTP status 404**. The server cannot find the requested URI (Uniform Resource Identifier). <br /> <br />|
|**0x80cf401A** <br /> <br />|OM_E_PT_HTTP_STATUS_BAD_METHOD <br /> <br />|Same as **HTTP status 405**. The HTTP method is not allowed. <br /> <br />|
|**0x80cf401B** <br /> <br />|OM_E_PT_HTTP_STATUS_PROXY_AUTH_REQ <br /> <br />|Same as **HTTP status 407**. Proxy authentication is required. <br /> <br />|
|**0x80cf401C** <br /> <br />|OM_E_PT_HTTP_STATUS_REQUEST_TIMEOUT <br /> <br />|Same as **HTTP status 408**. The server timed out waiting for the request. <br /> <br />|
|**0x80cf401D** <br /> <br />|OM_E_PT_HTTP_STATUS_CONFLICT <br /> <br />|Same as **HTTP status 409**. The request was not completed because of a conflict with the current state of the resource. <br /> <br />|
|**0x80cf401E** <br /> <br />|OM_E_PT_HTTP_STATUS_GONE <br /> <br />|Same as **HTTP status 410**. The requested resource is no longer available at the server. <br /> <br />|
|**0x80cf401F** <br /> <br />|OM_E_PT_HTTP_STATUS_SERVER_ERROR <br /> <br />|Same as **HTTP status 500**. An error internal to the server prevented the request from being fulfilled. <br /> <br />|
|**0x80cf4020** <br /> <br />|OM_E_PT_HTTP_STATUS_NOT_SUPPORTED <br /> <br />|Same as **HTTP status 500**. The server does not support the functionality that is required to fulfill the request. <br /> <br />|
|**0x80cf4021** <br /> <br />|OM_E_PT_HTTP_STATUS_BAD_GATEWAY <br /> <br />|Same as **HTTP status 502**. The server, while acting as a gateway or proxy, received an invalid response from the upstream server that it accessed while trying to fulfill the request. <br /> <br />|
|**0x80cf4022** <br /> <br />|OM_E_PT_HTTP_STATUS_SERVICE_UNAVAIL <br /> <br />|Same as **HTTP status 503**. The service is temporarily overloaded. <br /> <br />|
|**0x80cf4023** <br /> <br />|OM_E_PT_HTTP_STATUS_GATEWAY_TIMEOUT <br /> <br />|Same as **HTTP status 503**. The request was timed out waiting for a gateway. <br /> <br />|
|**0x80cf4024** <br /> <br />|OM_E_PT_HTTP_STATUS_VERSION_NOT_SUP <br /> <br />|Same as **HTTP status 505**. The server does not support the HTTP protocol version that is used for the request. <br /> <br />|
|**0x80cf4025** <br /> <br />|OM_E_PT_FILE_LOCATIONS_CHANGED <br /> <br />|The operation failed because of a changed file location. Refresh the internal state and resend. <br /> <br />|
|**0x80cf4027** <br /> <br />|OM_E_PT_NO_AUTH_PLUGINS_REQUESTED <br /> <br />|The server returned an empty authentication information list. <br /> <br />|
|**0x80cf4028** <br /> <br />|OM_E_PT_NO_AUTH_COOKIES_CREATED <br /> <br />|The agent could not create any valid authentication cookies. <br /> <br />|
|**0x80cf4029** <br /> <br />|OM_E_PT_INVALID_CONFIG_PROP <br /> <br />|A configuration property value was wrong. <br /> <br />|
|**0x80cf402A** <br /> <br />|OM_E_PT_CONFIG_PROP_MISSING <br /> <br />|A configuration property value was missing. <br /> <br />|
|**0x80cf402B** <br /> <br />|OM_E_PT_HTTP_STATUS_NOT_MAPPED <br /> <br />|The HTTP request could not be completed, and the reason did not correspond to any of the **OM_E_PT_HTTP_&#42;** error codes. <br /> <br />|
|**0x80cf402C** <br /> <br />|OM_E_PT_WINHTTP_NAME_NOT_RESOLVED <br /> <br />|Same as **ERROR_WINHTTP_NAME_NOT_RESOLVED**. The proxy server or destination server name cannot be resolved. <br /> <br />|
|**0x80cf402F** <br /> <br />|OM_E_PT_ECP_SUCCEEDED_WITH_ERRORS <br /> <br />|The external .cab file processing was completed with some errors. <br /> <br />|
|**0x80cf4030** <br /> <br />|OM_E_PT_ECP_INIT_FAILED <br /> <br />|The external .cab processor initialization was not completed. <br /> <br />|
|**0x80cf4031** <br /> <br />|OM_E_PT_ECP_INVALID_FILE_FORMAT <br /> <br />|The format of a metadata file is not valid. <br /> <br />|
|**0x80cf4032** <br /> <br />|OM_E_PT_ECP_INVALID_METADATA <br /> <br />|The external cab processor found metadata that is not valid. <br /> <br />|
|**0x80cf4033** <br /> <br />|OM_E_PT_ECP_FAILURE_TO_EXTRACT_DIGEST <br /> <br />|The file digest could not be extracted from an external .cab file. <br /> <br />|
|**0x80cf4034** <br /> <br />|OM_E_PT_ECP_FAILURE_TO_DECOMPRESS_CAB_FILE <br /> <br />|An external .cab file could not be decompressed. <br /> <br />|
|**0x80cf4035** <br /> <br />|OM_E_PT_ECP_FILE_LOCATION_ERROR <br /> <br />|The external cab processor could not get the file locations. <br /> <br />|
|**0x80cf4FFF** <br /> <br />|OM_E_PT_UNEXPECTED <br /> <br />|A communication error occurred that is not covered by another **OM_E_PT_&#42;** error code. <br /> <br />|
|**0x80cf6001** <br /> <br />|OM_E_DM_URLNOTAVAILABLE <br /> <br />|A download manager operation could not be completed because the requested file does not have a URL. <br /> <br />|
|**0x80cf6002** <br /> <br />|OM_E_DM_INCORRECTFILEHASH <br /> <br />|A download manager operation could not be completed because the file digest was not recognized. <br /> <br />|
|**0x80cf6003** <br /> <br />|OM_E_DM_UNKNOWNALGORITHM <br /> <br />|A download manager operation could not be completed because the file metadata requested an unrecognized hash algorithm. <br /> <br />|
|**0x80cf6005** <br /> <br />|OM_E_DM_NONETWORK <br /> <br />|A download manager operation could not be completed because the network connection was not available. <br /> <br />|
|**0x80cf6007** <br /> <br />|OM_E_DM_NOTDOWNLOADED <br /> <br />|The update has not been downloaded. <br /> <br />|
|**0x80cf6008** <br /> <br />|OM_E_DM_FAILTOCONNECTTOBITS <br /> <br />|A download manager operation failed because the download manager could not connect the Background Intelligent Transfer Service (BITS). <br /> <br />|
|**0x80cf6009** <br /> <br />|OM_E_DM_BITSTRANSFERERROR <br /> <br />|A download manager operation failed because there was an unspecified Background Intelligent Transfer Service (BITS) transfer error. <br /> <br />|
|**0x80cf600a** <br /> <br />|OM_E_DM_DOWNLOADLOCATIONCHANGED <br /> <br />|A download must be restarted because the download source location has changed. <br /> <br />|
|**0x80cf600B** <br /> <br />|OM_E_DM_CONTENTCHANGED <br /> <br />|A download must be restarted because the update content changed in a new revision. <br /> <br />|
|**0x80cf6FFF** <br /> <br />|OM_E_DM_UNEXPECTED <br /> <br />|A download manager error occurred that is not covered by another **OM_E_DM_&#42;** error code. <br /> <br />|
|**0x80cf7003** <br /> <br />|OM_E_INVALID_EVENT_PAYLOAD <br /> <br />|An event payload was specified that is not valid. <br /> <br />|
|**0x80cf7004** <br /> <br />|OM_E_INVALID_EVENT_PAYLOADSIZE <br /> <br />|The size of the event payload submitted is not valid. <br /> <br />|
|**0x80cf7005** <br /> <br />|OM_E_SERVICE_NOT_REGISTERED <br /> <br />|The service is not registered. <br /> <br />|
|**0x80cf8000** <br /> <br />|OM_E_DS_SHUTDOWN <br /> <br />|An operation failed because the agent is shutting down. <br /> <br />|
|**0x80cf8001** <br /> <br />|OM_E_DS_INUSE <br /> <br />|An operation failed because the data store was in use. <br /> <br />|
|**0x80cf8002** <br /> <br />|OM_E_DS_INVALID <br /> <br />|The current and expected states of the data store do not match. <br /> <br />|
|**0x80cf8003** <br /> <br />|OM_E_DS_TABLEMISSING <br /> <br />|The data store is missing a table. <br /> <br />|
|**0x80cf8004** <br /> <br />|OM_E_DS_TABLEINCORRECT <br /> <br />|The data store contains a table that has unexpected columns. <br /> <br />|
|**0x80cf8005** <br /> <br />|OM_E_DS_INVALIDTABLENAME <br /> <br />|A table could not be opened because the table is not in the data store. <br /> <br />|
|**0x80cf8006** <br /> <br />|OM_E_DS_BADVERSION <br /> <br />|The current and expected versions of the data store do not match. <br /> <br />|
|**0x80cf8007** <br /> <br />|OM_E_DS_NODATA <br /> <br />|The information that is requested is not in the data store. <br /> <br />|
|**0x80cf8008** <br /> <br />|OM_E_DS_MISSINGDATA <br /> <br />|The data store is missing required information or has a null in a table column that requires a non-null value. <br /> <br />|
|**0x80cf8009** <br /> <br />|OM_E_DS_MISSINGREF <br /> <br />|The data store is missing required information or has a reference to missing license terms, file, localized property, or linked row. <br /> <br />|
|**0x80cf800A** <br /> <br />|OM_E_DS_UNKNOWNHANDLER <br /> <br />|The update was not processed because its update handler was not recognized. <br /> <br />|
|**0x80cf800B** <br /> <br />|OM_E_DS_CANTDELETE <br /> <br />|The update was not deleted because it is still referenced by one or more services. <br /> <br />|
|**0x80cf800C** <br /> <br />|OM_E_DS_LOCKTIMEOUTEXPIRED <br /> <br />|The data store section could not be locked within the allotted time. <br /> <br />|
|**0x80cf800E** <br /> <br />|OM_E_DS_ROWEXISTS <br /> <br />|The row was not added because an existing row has the same primary key. <br /> <br />|
|**0x80cf800F** <br /> <br />|OM_E_DS_STOREFILELOCKED <br /> <br />|The data store could not be initialized because it was locked by another process. <br /> <br />|
|**0x80cf8010** <br /> <br />|OM_E_DS_CANNOTREGISTER <br /> <br />|The data store is not allowed to be registered with COM in the current process. <br /> <br />|
|**0x80cf8011** <br /> <br />|OM_E_DS_UNABLETOSTART <br /> <br />|An operation could not create a data store object in another process. <br /> <br />|
|**0x80cf8013** <br /> <br />|OM_E_DS_DUPLICATEUPDATEID <br /> <br />|The server sent the same update to the client with two different revision IDs. <br /> <br />|
|**0x80cf8014** <br /> <br />|OM_E_DS_UNKNOWNSERVICE <br /> <br />|An operation could not be completed because the service is not in the data store. <br /> <br />|
|**0x80cf8015** <br /> <br />|OM_E_DS_SERVICEEXPIRED <br /> <br />|An operation could not be completed because the registration of the service has expired. <br /> <br />|
|**0x80cf8016** <br /> <br />|OM_E_DS_DECLINENOTALLOWED <br /> <br />|A request to hide an update was declined because it is a mandatory update or because it was deployed with a deadline. <br /> <br />|
|**0x80cf8017** <br /> <br />|OM_E_DS_TABLESESSIONMISMATCH <br /> <br />|A table was not closed because it is not associated with the session. <br /> <br />|
|**0x80cf8018** <br /> <br />|OM_E_DS_SESSIONLOCKMISMATCH <br /> <br />|A table was not closed because it is not associated with the session. <br /> <br />|
|**0x80cf8019** <br /> <br />|OM_E_DS_NEEDWINDOWSSERVICE <br /> <br />|The request to remove or unregister the service was declined because it is a built-in service or because Automatic Updates cannot fall back to another service. <br /> <br />|
|**0x80cf801A** <br /> <br />|OM_E_DS_INVALIDOPERATION <br /> <br />|The request was declined because the operation is not allowed. <br /> <br />|
|**0x80cf801B** <br /> <br />|OM_E_DS_SCHEMAMISMATCH <br /> <br />|The schema of the current data store and the schema of a table in a backup XML document do not match. <br /> <br />|
|**0x80cf801C** <br /> <br />|OM_E_DS_RESETREQUIRED <br /> <br />|The data store requires a session reset. Release the session and retry with a new session. <br /> <br />|
|**0x80cf801D** <br /> <br />|OM_E_DS_IMPERSONATED <br /> <br />|A data store operation could not be completed because it was requested with an impersonated identity. <br /> <br />|
|**0x80cf8FFF** <br /> <br />|OM_E_DS_UNEXPECTED <br /> <br />|A data store error occurred that is not covered by another **OM_E_DS_&#42;** code. <br /> <br />|
|**0x80cfA000** <br /> <br />|OM_E_AU_NOSERVICE <br /> <br />|Automatic Updates could not service incoming requests. <br /> <br />|
|**0x80cfA004** <br /> <br />|OM_E_AU_PAUSED <br /> <br />|Automatic Updates could not process incoming requests because it was paused. <br /> <br />|
|**0x80cfA005** <br /> <br />|OM_E_AU_NO_REGISTERED_SERVICE <br /> <br />|No unmanaged service is registered with Automatic Updates. <br /> <br />|
|**0x80cfA006** <br /> <br />|OM_E_AU_DETECT_SVCID_MISMATCH <br /> <br />|The default service registered with Automatic Updates changed during the search. <br /> <br />|
|**0x80cfA007** <br /> <br />|OM_E_AU_ALREADY_PROMPTING_FOR_REBOOT <br /> <br />|Automatic Updates is already prompting the user to restart. <br /> <br />|
|**0x80cfAFFF** <br /> <br />|OM_E_AU_UNEXPECTED <br /> <br />|An Automatic Updates error occurred that is not covered by another **OM_E_AU &#42;** code. <br /> <br />|
|**0x80cfE001** <br /> <br />|OM_E_EE_UNKNOWN_EXPRESSION <br /> <br />|An expression evaluator operation could not be completed because an expression was not recognized. <br /> <br />|
|**0x80cfE002** <br /> <br />|OM_E_EE_INVALID_EXPRESSION <br /> <br />|An expression evaluator operation could not be completed because an expression was not valid. <br /> <br />|
|**0x80cfE003** <br /> <br />|OM_E_EE_MISSING_METADATA <br /> <br />|An expression evaluator operation could not be completed because an expression contains an incorrect number of metadata nodes. <br /> <br />|
|**0x80cfE004** <br /> <br />|OM_E_EE_INVALID_VERSION <br /> <br />|An expression evaluator operation could not be completed because the version of the serialized expression data is not valid. <br /> <br />|
|**0x80cfE005** <br /> <br />|OM_E_EE_NOT_INITIALIZED <br /> <br />|The expression evaluator could not be initialized. <br /> <br />|
|**0x80cfE006** <br /> <br />|OM_E_EE_INVALID_ATTRIBUTEDATA <br /> <br />|An expression evaluator operation could not be completed because an attribute is not valid. <br /> <br />|
|**0x80cfE007** <br /> <br />|OM_E_EE_CLUSTER_ERROR <br /> <br />|An expression evaluator operation could not be completed because the cluster state of the computer could not be determined. <br /> <br />|
|**0x80cfEFFF** <br /> <br />|OM_E_EE_UNEXPECTED <br /> <br />|An expression evaluator error occurred that is not covered by another **OM_E_EE_&#42;** error code. <br /> <br />|
|**0x80cfF001** <br /> <br />|OM_E_REPORTER_EVENTCACHECORRUPT <br /> <br />|The event cache file was defective. <br /> <br />|
|**0x80cfF002** <br /> <br />|OM_E_REPORTER_EVENTNAMESPACEPARSEFAILED <br /> <br />|The XML in the event namespace descriptor could not be parsed. <br /> <br />|
|**0x80cfF003** <br /> <br />|OM_E_INVALID_EVENT <br /> <br />|The XML in the event namespace descriptor is not valid. <br /> <br />|
|**0x80cfF004** <br /> <br />|OM_E_SERVER_BUSY <br /> <br />|The server rejected an event because the server was too busy. <br /> <br />|
|**0x80cfFFFF** <br /> <br />|OM_E_REPORTER_UNEXPECTED <br /> <br />|A reporter error occurred that is not covered by another error code. <br /> <br />|
|**0x80af0005** <br /> <br />|OMC_E_INSTALL_NOT_ALLOWED_REBOOT_REQUIRED <br /> <br />|Installation failed because there is a pending mandatory reboot. <br /> <br />|
|**0x80af0006** <br /> <br />|OMC_E_DOWNLOAD_CANCELLED <br /> <br />|The download was canceled. <br /> <br />|
