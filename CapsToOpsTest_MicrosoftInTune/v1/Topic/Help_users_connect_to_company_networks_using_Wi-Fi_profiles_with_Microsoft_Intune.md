Use [!INC[wit_firstref](../Token/wit_firstref_md.md)] Wi-Fi profiles to deploy wireless network settings to users and devices in your organization. These settings simplify connecting to wireless networks for end-users.

For example:

- You install a new Wi-Fi network named **Contoso Wi-Fi** and want to provision all devices that run the iOS operating system with the settings required to connect to this network.

- You create a Wi-Fi profile containing the settings necessary to connect to the **Contoso Wi-Fi** wireless network.

- You then deploy this profile to all users with iOS devices.

- Users find the new **Contoso Wi-Fi** network in the list of wireless networks and can easily connect to this network.

You can deploy Wi-Fi profiles to the following platforms:

- Android 4.0 and later

- iOS 7.1 and later

- Mac OS X 10.9 and later

Additionally, for devices that run Windows 8.1 and later, you can import a Wi-Fi configuration profile that was previously exported to a file. For details, see [Import a Wi-Fi configuration profile (Windows 8.1 and later only)](../Topic/Help_users_connect_to_company_networks_using_Wi-Fi_profiles_with_Microsoft_Intune.md#BKMK_Import).

## Steps to create and deploy a Wi-Fi profile

### Step 1: Create a Wi-Fi profile and supply general information

1. In the [Microsoft Intune administration console](https://manage.microsoft.com), click **Policy** &gt; **Add Policy**.

2. Select one of the following policy types, and then click **Create Policy**:

   - **Wi-Fi Profile (Android 4 and later)**

   - **Wi-Fi Profile (iOS 7.1 and later)**

   - **Wi-Fi Profile (Mac OS X 10.9 and later)**

   There are no recommended settings for this policy type. You must create a custom policy.

3. Specify the following general values:

   |Setting <br /> <br />|More information <br /> <br />|
   |-----------|--------------------|
   |**Name** <br /> <br />|Enter a unique name for the Wi-Fi profile to help identify it in the [!INC[wit_nextref](../Token/wit_nextref_md.md)] console. <br /> <br />|
   |**Description** <br /> <br />|Provide a description of the Wi-Fi profile that helps you to locate it. <br /> <br />|

### Step 2: Configure network connection settings
Specify the **Network Connections** values:

|Setting <br /> <br />|More information <br /> <br />|
|-----------|--------------------|
|**Network name** <br /> <br />|Specify a descriptive name for the wireless network. This is the name that displays on a user’s device when they choose a wireless network. <br /> <br />|
|**SSID (Service Set Identifier)** <br /> <br />|Specify the (SSID) of the wireless network that you want devices to connect to. The SSID is case-sensitive and is not displayed to users. <br /> <br />|
|**Connect automatically when this network is in range** <br /> <br />|Select this option to automatically connect devices to the wireless network when it is in range. <br /> <br />|
|**Connect when the network is not broadcasting its name (SSID)** <br /> <br />|Select this option to allow devices to connect to the network when it is not visible in the list of networks (because it is hidden and not broadcasting its name). <br /> <br />|

### Step 3: Configure security settings
Configure the **Security Settings** for the selected platform. The available settings depend on the security types you select.

#### For Android devices

|Setting name <br /> <br />|More information <br /> <br />|Use when: <br /> <br />|
|----------------|--------------------|-------------|
|**Security type** <br /> <br />|Select the security protocol for the wireless network: <br /> <br /><ul><li>**WPA-Enterprise/WPA2-Enterprise** </li><li>**No authentication (Open)** if the network is unsecured. </li> </ul>|Always <br /> <br />|
|**EAP Type** <br /> <br />|Choose the Extensible Authentication Protocol (EAP) type used to authenticate secured wireless connections: <br /> <br /><ul><li>**EAP-TLS** </li><li>**PEAP** </li><li>**EAP-TTLS** </li> </ul>|You selected the **WPA-Enterprise/WPA2-Enterprise** security type. <br /> <br />|
|**Select root certificates for server validation** <br /> <br />|Click **Select**, then choose the trusted root certificate profile used to authenticate the connection. **Important:** To create the trusted root certificate profile, see [Enable access to company resources using certificate profiles with Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md). <br />|Any **EAP Type** is selected. <br /> <br />|
|**Authentication method** <br /> <br />|Select the authentication method for the connection: <br /> <br /><ul><li>**Certificates** to specify the client certificate </li><li>**Username and Password** to specify a different method for authentication </li> </ul>|The **EAP type** is **PEAP** or **EAP-TTLS**. <br /> <br />|
|**Select a non-EAP method for authentication (Inner identity)** <br /> <br />|Select how you will authenticate the connection: <br /> <br /><ul><li>**None** </li><li>**Unencrypted password (PAP)** </li><li>**Challenge Handshake Authentication Protocol (CHAP)** </li><li>**Microsoft CHAP (MS-CHAP)** </li><li>**Microsoft CHAP Version 2 (MS-CHAP v2)** </li> </ul>The available options depend on the EAP type you selected. <br /> <br />|The **Authentication method** is **Username and Password**. <br /> <br />|
|**Enable identity privacy (Outer Identity)** <br /> <br />|Specify the text sent in response to an EAP identity request. This text can be any value. During authentication, this anonymous identity is initially sent, and then followed by the real identification sent in a secure tunnel. <br /> <br />|The **EAP type** is **PEAP** or **EAP-TTLS**. <br /> <br />|
|**Select a client certificate for client authentication (Identity Certificate)** <br /> <br />|Click **Select**, then choose the SCEP certificate profile used to authenticate the connection. **Important:** To create a SCEP certificate profile, see [Enable access to company resources using certificate profiles with Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md). <br />|The security type is **WPA-Enterprise/WPA2-Enterprise**, and any **EAP type** is selected. <br /> <br />|

#### For iOS and Mac OS X devices

|Setting name <br /> <br />|More information <br /> <br />|Use when: <br /> <br />|
|----------------|--------------------|-------------|
|**Security type** <br /> <br />|Select the wireless network security protocol: <br /> <br /><ul><li>**WPA-Personal/WPA2-Personal** </li><li>**WPA-Enterprise/WPA2-Enterprise** </li><li>**WEP** </li><li>**No authentication (Open)** if the network is unsecured. </li> </ul>|Always <br /> <br />|
|**EAP Type** <br /> <br />|Choose the Extensible Authentication Protocol (EAP) type used to authenticate secured wireless connections: <br /> <br /><ul><li>**EAP-TLS** </li><li>**PEAP** </li><li>**EAP-TLS** </li><li>**EAP-AST** </li><li>**LEAP** </li><li>**EAP-SIM** </li> </ul>|You selected a security type of **WPA-Enterprise/WPA2-Enterprise**. <br /> <br />|
|**Trusted server certificate names** <br /> <br />|Select the trusted root certificate profile used to authenticate the connection. **Important:** To create the trusted root certificate profile, see [Enable access to company resources using certificate profiles with Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md). <br />|You selected an EAP type of **EAP-TLS**, **PEAP**, **EAP-TTLS** or **EAP-FAST**. <br /> <br />|
|**Use Protected Access Credential (PAC)** <br /> <br />|Select to use protected access credentials to establish an authenticated tunnel between the client and the authentication server. An existing PAC file is used if present. <br /> <br />|The **EAP-type** is **EAP-FAST**. <br /> <br />|
|**Provision PAC** <br /> <br />|Provisions the PAC file to your devices. <br /> <br />When used, you can also select **Provision PAC Anonymously** to ensure that the PAC file is provisioned without authenticating the server. <br /> <br />|**Use Protected Access Credential (PAC)** is selected. <br /> <br />|
|**Authentication method** <br /> <br />|Select the authentication method used for the connection: <br /> <br /><ul><li>**Certificates** to specify the client certificate </li><li>**Username and Password** to specify one of the following non-EAP methods for authentication (also known as Inner identity): <br /> <br /><ul><li>**None** </li><li>**Unencrypted password (PAP)** </li><li>**Challenge Handshake Authentication Protocol (CHAP)** </li><li>**Microsoft CHAP (MS-CHAP)** </li><li>**Microsoft CHAP Version 2 (MS-CHAP v2)** </li><li>**EAP-TLS** </li> </ul> </li> </ul>|The **EAP type** is **PEAP**, or **EAP-TTLS**. <br /> <br />|
|**Select a client certificate for client authentication (Identity Certificate)** <br /> <br />|Select the SCEP certificate profile used to authenticate the connection. **Important:** To create a SCEP certificate profile, see [Enable access to company resources using certificate profiles with Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md). <br />|When the security type is **WPA-Enterprise/WPA2-Enterprise** and the **EAP type** is **EAP-TLS**, **PEAP** or **EAP-TTLS**. <br /> <br />|
|**Enable identity privacy (Outer Identity)** <br /> <br />|Specify text that sent in response to an EAP identity request. This text can be any value. <br /> <br />During authentication, this anonymous identity is initially sent, followed by the real identification sent in a secure tunnel. <br /> <br />|When the **EAP type** is set to **PEAP**, **EAP-TTLS** or **EAP-FAST**. <br /> <br />|

### Step 4: Configure proxy settings (iOS and MAC OS X only)

1. For iOS and Mac OS X Wi-Fi profiles, configure the following settings (if you are using a proxy server to help secure your network) under **Proxy Settings**:

   |Setting name <br /> <br />|Moe information <br /> <br />|Use when: <br /> <br />|
   |----------------|-------------------|-------------|
   |**Proxy settings for this Wi-Fi connection** <br /> <br />|Choose the proxy settings type: <br /> <br /><ul><li>**None** (default) </li><li>**Manual** -   Manually specify the URL and port number of the proxy server. </li><li>**Automatic** – Use a configuration file to configure the proxy server. </li> </ul>|Always <br /> <br />|
   |**Proxy server address** and **Port number** <br /> <br />|Specify the URL and port number of the proxy server. <br /> <br />|**Proxy settings for this Wi-Fi connection** is set to **Manual** <br /> <br />|
   |**Proxy Server URL** <br /> <br />|Specify the URL of the file containing the proxy server settings. <br /> <br />|**Proxy settings for this Wi-Fi connection** is set to **Automatic** <br /> <br />|

### Step 5: Save the Wi-Fi profile

1. When you are finished, click **Save Policy**.

The new policy displays in the **Configuration Policies** node of the **Policy** workspace.

### Step 6: Deploy the Wi-Fi profile

1. Deploy the Wi-Fi profile to one or more groups of users or devices in your organization.

For more information about how to deploy policies, see [Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

A status summary and alerts in the **Policy** workspace identify issues with the policy that require your attention. Additionally, a status summary appears in the **Dashboard** workspace.

After successful deployment, users devices can automatically connect to the corporate wireless network you configured.

## <a name="BKMK_Import"></a>Import a Wi-Fi configuration profile (Windows 8.1 and later only)
Use the **Windows Wi-Fi Import Policy** to import a set of Wi-Fi settings that you can then deploy to the required user or device groups.

> [!TIP]
> In Windows, you can use the **netsh wlan** utility to export an existing Wi-Fi profile to an XML file readable by [!INC[wit_nextref](../Token/wit_nextref_md.md)].
> 
> For example, to export a Wi-Fi connection named **MyConnection** to an XML file, type the following from a Windows command prompt:
> 
> **netsh wlan export profile MyConnection**

1. In the [Microsoft Intune administration console](https://manage.microsoft.com), click **Policy** &gt; **Add Policy**.

2. Configure a policy of the type **Windows** &gt; **Windows Wi-Fi Import Policy**.

   You can only create and deploy a custom Windows Wi-Fi import policy. Recommended settings are not available.

   For more information about how to create and deploy policies, see the [Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md) topic.

3. Specify the following general values for the Windows Wi-Fi Import Policy:

   |Setting name <br /> <br />|More information <br /> <br />|
   |----------------|--------------------|
   |**Name** <br /> <br />|Enter a unique name for the Wi-Fi profile to identify it in the [!INC[wit_nextref](../Token/wit_nextref_md.md)] console. <br /> <br />|
   |**Description** <br /> <br />|Provide a description w of the Wi-Fi profile and other relevant information that helps you to locate it. <br /> <br />|

4. Specify the following values under the **Custom Wi-Fi Profile** heading:

   |Setting name <br /> <br />|More information <br /> <br />|
   |----------------|--------------------|
   |**Configuration profile file** <br /> <br />|Click **Import** to select the XML file containing the Wi-Fi profile settings that you want to import into [!INC[wit_nextref](../Token/wit_nextref_md.md)]. <br /> <br />|
   |**Custom configuration profile name (displayed to users)** <br /> <br />|Displays the name of the Wi-Fi configuration profile as it will be shown to users on their device. <br /> <br />|
   |**Configuration profile details** <br /> <br />|Displays the XML code for the configuration profile you selected. <br /> <br />|

5. When you are finished, click **Save Policy**.

6. The new policy displays in the **Configuration Policies** node of the **Policy** workspace.

You can now use the information in **Step 6** above to help you deploy the custom Wi-Fi profile.

## See Also
[Enable access to company resources with Microsoft Intune](http://msdn.microsoft.com/en-us/library/5b090c5a-6f12-4e60-ace0-c9929afaa9a3)

