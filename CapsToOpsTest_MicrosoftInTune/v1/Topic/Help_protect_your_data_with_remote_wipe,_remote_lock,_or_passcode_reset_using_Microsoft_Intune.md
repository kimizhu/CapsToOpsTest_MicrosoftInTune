<?xml version="1.0" encoding="utf-8"?>
<developerHowToDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd">
  <introduction>
    <para>
      <token>wit_firstref</token> provides selective wipe, full wipe, remote lock, and passcode reset capabilities. Because mobile devices can store sensitive corporate data and provide access to many corporate resources, you can issue a remote device wipe command from the <token>wit_adminconsole</token> to wipe a lost or stolen device. Also, users can issue a remote device wipe command from the <token>wit_iwportal_1</token> on privately owned devices enrolled in Intune. </para>
    
    <alert class="note">
 <para>This topic is only about wiping devices managed by Intune. You can also use <externalLink><linkText>the Azure preview portal</linkText><linkUri>https://portal.azure.com</linkUri></externalLink> to <externalLink><linkText>wipe company data from apps</linkText><linkUri>https://technet.microsoft.com/en-us/library/mt627826.aspx</linkUri></externalLink>.</para>
</alert></introduction>
  <section address="bkmk_wipe">
    <title>Use Retire/Wipe to help secure a lost device or to retire a device from active use</title>
    <content>
      
      <para><ui>Full wipe</ui> restores a device to its factory default settings, removing all company and user data and settings.     The device is removed from Intune. <ui>Be careful about selecting full wipe; your data cannot be recovered</ui>.</para>
      <para><ui>Selective wipe</ui> removes company data from a device.   The device is removed from Intune. The following tables describe by platform what data is removed and the effect on data that remains on the device after a selective wipe. </para>
      <para><ui>iOS</ui></para><table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
        <thead>
          <tr>
            <TD>
              <para>Data type</para>
            </TD>
            
            
            
            <TD>
              <para>iOS</para>
            </TD>
            
            
          </tr>
        </thead>
        <tbody>
          <tr>
            <TD>
              <para>Company apps and associated data installed by <token>wit_firstref</token>.</para>
            </TD>
            
            
            
            <TD>
              <para>Apps are uninstalled. Company app data is removed.</para>
              <para>App data from Microsoft apps that use mobile app management is removed. The app is not removed.</para>
            </TD>
            
            
          </tr>
          <tr>
            <TD>
              <para>Settings</para>
            </TD>
            <TD><para>Configurations that were set by <token>wit_nextref</token> policy are no longer enforced and users can change the settings.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>Wi-Fi and VPN profile settings</para>
            </TD>
            
            
            
            <TD>
              <para>Removed</para>
            </TD>
            
            
          </tr>
          <tr>
            <TD>
              <para>Certificate profile settings</para>
            </TD>
            
            
            
            <TD>
              <para>Certificates removed and revoked.</para>
            </TD>
            
            
          </tr>
          <tr>
            <TD>
              <para>Management Agent</para>
            </TD>
            
            
            
            <TD>
              <para>Management profile is removed.</para>
            </TD>
            
            
          </tr>
          <tr>
            <TD>
              <para>Email</para>
            </TD>
            
            
            
            <TD>
              <para>Email profiles that are provisioned through <token>wit_nextref</token> are removed and cached email on the device is deleted.</para>
            </TD>
            
            
          </tr>
          <tr>
            <TD>
              <para>Azure Active Directory (AAD) Unjoin</para>
            </TD>
            
            
            
            <TD>
              <para>AAD Record removed</para>
            </TD>
            
            
          </tr>
        </tbody>
      </table>
      <para></para><para><ui>Android</ui></para><table>
        <thead>
          <tr>
            <TD>
              <para>Data type</para>
            </TD>
            
            
            
            
            <TD>
              <para>Android</para>
            </TD>
            <TD>
              <para>Android Samsung KNOX</para>
            </TD>
          </tr>
        </thead>
        <tbody>
          
          <tr><TD><para>Web links</para></TD><TD><para>Removed.</para></TD><TD><para>Removed</para></TD></tr><tr><TD><para>Unmanaged Google Play apps</para></TD><TD><para>Apps and data remain installed</para></TD><TD><para>Apps and data remain installed</para></TD></tr><tr><TD><para>Unmanaged line of business apps</para></TD><TD><para>Apps and data remain installed</para></TD><TD><para>Apps are uninstalled and data local to app is removed as a result. No data outside the app (SD card, etc.) is removed.</para></TD></tr><tr><TD><para>Managed Google Play apps</para></TD><TD><para>App data is removed. App is not removed. Data protected by MAM encryption outside the app (SD card, etc.) remain encrypted but aren't removed.</para></TD><TD><para>App data is removed. App is not removed. Data protected by MAM encryption outside the app (SD card, etc.) remain encrypted but aren't removed.</para></TD></tr><tr><TD><para>Managed line of business apps</para></TD><TD><para>App data is removed. App is not removed. Data protected by MAM encryption outside the app (SD card, etc.) remain encrypted but aren't removed.</para></TD><TD><para>App data is removed. App is not removed. Data protected by MAM encryption outside the app (SD card, etc.) remain encrypted but aren't removed.</para></TD></tr><tr>
            <TD>
              <para>Settings</para>
            </TD>
            <TD colspan="2"><para>Configurations that were set by <token>wit_nextref</token> policy are no longer enforced and users can change the settings.</para>
            
            </TD>
          </tr>
          <tr>
            <TD>
              <para>Wi-Fi and VPN profile settings</para>
            </TD>
            
            
            
            
            <TD>
              <para>Removed</para>
            </TD>
            <TD>
              <para>Removed</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>Certificate profile settings</para>
            </TD>
            
            
            
            
            <TD>
              <para>Certificates revoked, but not removed.</para>
            </TD>
            <TD>
              <para>Certificates removed and revoked.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>Management Agent</para>
            </TD>
            
            
            
            
            <TD>
              <para>Device Administrator privilege is revoked.</para>
            </TD>
            <TD>
              <para>Device Administrator privilege is revoked.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>Email</para>
            </TD>
            
            
            
            
            <TD>
              <para>Email  received by the Microsoft Outlook app for Android  app is removed.</para>
            </TD>
            <TD>
              <para>Email profiles that are provisioned through <token>wit_nextref</token> are removed and cached email on the device is deleted.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>Azure Active Directory (AAD) Unjoin</para>
            </TD>
            
            
            
            
            <TD>
              <para>AAD Record removed</para>
            </TD>
            <TD>
              <para>AAD Record removed</para>
            </TD>
          </tr>
        </tbody>
      </table><para></para><para><ui>Windows</ui></para><table>
        <thead>
          <tr>
            <TD>
              <para>Data type</para>
            </TD>
            <TD>
              <para>Windows 8.1 (enrolled as a mobile device) and Windows RT 8.1</para>
            </TD>
            <TD>
              <para>Windows RT</para>
            </TD>
            <TD>
              <para>Windows Phone 8 and Windows Phone 8.1</para>
            </TD>
            
            
            
          </tr>
        </thead>
        <tbody>
          <tr>
            <TD>
              <para>Company apps and associated data installed by <token>wit_firstref</token>.</para>
            </TD>
            <TD>
              <para>Files protected by EFS will have their key revoked and the user will not be able to open the files.</para>
            </TD>
            <TD>
              <para>Will not remove company apps.</para>
            </TD>
            <TD>
              <para>Apps originally installed through the company portal are uninstalled. Company app data is removed.</para>
            </TD>
            
            
            
          </tr>
          <tr><TD>
              <para>Settings</para>
            </TD>
            
            <TD colspan="3">
              <para>Configurations that were set by <token>wit_nextref</token> policy are no longer enforced and users can change the settings.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>Wi-Fi and VPN profile settings</para>
            </TD>
            <TD>
              <para>Removed</para>
            </TD>
            <TD>
              <para>Removed</para>
            </TD>
            <TD>
              <para>Not supported</para>
            </TD>
            
            
            
          </tr>
          <tr>
            <TD>
              <para>Certificate profile settings</para>
            </TD>
            <TD>
              <para>Certificates removed and revoked.</para>
            </TD>
            <TD>
              <para>Certificates removed and revoked.</para>
            </TD>
            <TD>
              <para>Not supported</para>
            </TD>
            
            
            
          </tr>
          <tr>
            <TD>
              <para>Management Agent</para>
            </TD>
            <TD>
              <para>Not applicable. Management agent is built-in.</para>
            </TD>
            <TD>
              <para>Not applicable. Management agent is built-in.</para>
            </TD>
            <TD>
              <para>Not applicable. Management agent is built-in.</para>
            </TD>
            
            
            
          </tr>
          <tr>
            <TD>
              <para>Email</para>
            </TD>
            <TD>
              <para>Removes email that is EFS enabled which includes the Mail app for Windows email and attachments.</para>
            </TD>
            <TD>
              <para>Not supported</para>
            </TD>
            <TD>
              <para>Email profiles that are provisioned through <token>wit_nextref</token> are removed and cached email on the device is deleted.</para>
            </TD>
            
            
            
          </tr>
          <tr>
            <TD>
              <para>Azure Active Directory (AAD) Unjoin</para>
            </TD>
            <TD>
              <para>No</para>
            </TD>
            <TD>
              <para>No</para>
            </TD>
            <TD>
              <para>AAD Record removed</para>
            </TD>
            
            
            
          </tr>
        </tbody>
      </table><procedure>
        <title>To remotely wipe a device from the Intune administrator console</title>
        <steps class="ordered">
          <step>
            <content>
              <para>Select devices to be wiped. You can find them either by user or by device.</para><list class="bullet"><listItem><para><embeddedLabel>By user:</embeddedLabel></para><list class="ordered"><listItem><para>In the <externalLink><linkText>Intune administrator console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Groups</ui> &gt; <ui>All Users</ui>. </para></listItem><listItem><para>Click the name of the user whose mobile device you want to wipe. Click <ui>View Properties</ui>.</para></listItem><listItem><para>On the user's <ui>Properties </ui> page, click <ui>Devices</ui>, and then click the name of the mobile device you want to wipe. Use Ctrl+click to multi-select devices.</para></listItem></list></listItem><listItem><para><embeddedLabel>By device:</embeddedLabel></para><list class="ordered"><listItem><para>In the <externalLink><linkText>Intune administrator console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Groups</ui> &gt; <ui>All Mobile Devices</ui>. </para></listItem><listItem><para>Click <ui>Devices</ui>, and then click the name of the mobile device you want to wipe. Use Ctrl+click to multi-select devices.</para></listItem></list></listItem></list>
            </content>
          </step>
          
          
          <step>
            <content>
              <para>Click <ui>Retire/Wipe</ui>. </para>
            </content>
          </step>
          <step>
            <content>
              <para>A message appears, prompting you to confirm whether you want to retire the device.</para>
              <list class="bullet">
                <listItem>
                  <para>To perform a <embeddedLabel>Selective wipe</embeddedLabel> which only removes company apps and data, click <ui>Yes</ui>.</para>
                </listItem>
                <listItem>
                  <para>To perform a <embeddedLabel>Full wipe</embeddedLabel> that erases all apps and data and returns the device to factory default settings, select <ui>Wipe the device before retiring</ui>. This action applies to all platforms except Windows 8.1. <ui>You cannot recover data removed by a full wipe</ui>.</para>
                </listItem>
              </list>
            </content>
          </step>
        </steps>
        <conclusion>
          <content>
            <para>It takes less than 15 minutes for a wipe to propagate across all device types.</para>
          </content>
        </conclusion>
      </procedure>
    </content>
    <sections>
      <section>
        <title>Wiping Encryption File System (EFS)-enabled content</title>
        <content>
          <para>Selective wipe of EFS-encrypted content is supported by Windows 8.1 and Windows RT 8.1. The following apply to a selective wipe of EFS-enabled content:</para>
          <list class="bullet">
            <listItem>
              <para>Only apps and data that are protected by EFS using the same Internet domain as the <token>wit_nextref</token> account are selectively wiped. For more information, see <externalLink><linkText>Windows Selective Wipe for Device Data Management</linkText><linkUri>http://technet.microsoft.com/library/dn486874.aspx</linkUri></externalLink>.</para>
            </listItem>
            <listItem>
              <para>If there are any changes are made to the domain associated with EFS, the changes can take up to 48 hours before apps and data using the new domain can be selectively wiped.</para>
            </listItem>
            <listItem>
              <para>Each domain that is registered with <token>wit_nextref</token> will be wiped.</para>
            </listItem>
          </list>
          <para>The data and apps that are currently supported by EFS selective wipe are:</para>
          <list class="bullet">
            <listItem>
              <para>Mail app for Windows</para>
            </listItem>
            <listItem>
              <para>Work Folders</para>
            </listItem>
            <listItem>
              <para>Files and folders encrypted by EFS. For more information, see <externalLink><linkText>Best practices for the Encrypting File System</linkText><linkUri>http://support.microsoft.com/kb/223316</linkUri></externalLink>.</para>
            </listItem>
            <listItem>
              <para>If your organization maintains its identity in Active Directory, it must use the Directory Sync (DirSync) tool to sync information into AAD for EFS selective wipe to work correctly.  For more information on DirSync, see <externalLink><linkText>Directory Sync Scenario</linkText><linkUri>http://technet.microsoft.com/library/dn441212.aspx</linkUri></externalLink> in the Azure Active Directory documentation.</para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>Monitor retire, wipe, and delete actions</title>
        <content>
          <para>To get a report of devices that have been retired, wiped, or deleted, and who performed the action:</para><procedure>
            <title/>
            <steps class="ordered">
              <step>
                <content>
                  <para>In the <externalLink><linkText>Intune administrator  console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Reports</ui> &gt; <ui>Device History Reports</ui>.</para>
                </content>
              </step>
              <step>
                <content>
                  <para>Provide a start and end date for the report, then click <ui>View Report</ui>.</para>
                </content>
              </step>
            </steps>
            
              
                
          </procedure>
        </content>
      </section>
    <section address="BKMK_passcode">
        <title>Reset the passcode on a device</title>
        <content>
            <para>If a user forgets their passcode, you can help them by removing the passcode from a device or by forcing a new temporary passcode on a device. The table below lists how passcode reset works on different mobile platforms.</para>
      <table>
        <thead>
          <tr>
            <TD>
              <para>Platform</para>
            </TD>
            <TD>
              <para>Passcode reset</para>
            </TD>
          </tr>
        </thead>
        <tbody>
          <tr>
            <TD>
              <para>iOS</para>
            </TD>
            <TD>
              <para>Supported for clearing the passcode from a device. Does not create a new temporary passcode.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>Android</para>
            </TD>
            <TD>
              <para>Supported and a temporary passcode is created.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>Windows Phone 8 and Windows Phone 8.1</para>
            </TD>
            <TD>
              <para>Supported</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <token>winblue_winrt_2</token> and <token>win8RT_client_1</token></para>
            </TD>
            <TD>
              <para>Not Supported</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>Windows 8.1</para>
            </TD>
            <TD>
              <para>Not Supported</para>
            </TD>
          </tr>
        </tbody>
      </table>
      <procedure>
        <title>To reset the passcode on a mobile device remotely through the Microsoft Intune console</title>
        <steps class="ordered">
          <step>
            <content>
              <para>In the <externalLink><linkText>Intue administrator  console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Groups</ui> &gt; <ui>All Devices</ui> &gt; <ui>All Mobile Devices</ui>.</para>
            </content>
          </step>
          <step>
            <content>
              <para>Click <ui>All Direct Managed Devices</ui> for devices enrolled in Intune or <ui>All Exchange ActiveSync Managed Devices</ui>.</para>
              <alert class="tip">
                <para>You can also navigate to a device by user. Click <ui>All Users</ui>. On the user's properties page, click <ui>Devices</ui>, and then click the name of the mobile device you want to wipe.</para>
              </alert>
            </content>
          </step>
          <step>
            <content>
              <para>In the list, click the device or devices that you want to lock. On the taskbar, click <ui>Remote Tasks</ui>, and select <ui>Passcode Reset</ui>.</para>
            </content>
          </step>
        </steps>
      </procedure></content>
        
    </section><section>
                <title> Lock a device remotely</title>
                <content>
                    <para>If a user loses their device you can lock the device remotely. The table below lists how remote lock works on different mobile platforms.</para>
      <table>
        <thead>
          <tr>
            <TD>
              <para>Platform</para>
            </TD>
            <TD>
              <para>Remote lock</para>
            </TD>
          </tr>
        </thead>
        <tbody>
          <tr>
            <TD>
              <para>iOS</para>
            </TD>
            <TD>
              <para>Supported</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>Android</para>
            </TD>
            <TD>
              <para>Supported</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>Windows Phone 8 and Windows Phone 8.1</para>
            </TD>
            <TD>
              <para>Supported</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>
                <token>winblue_winrt_2</token> and <token>win8RT_client_1</token></para>
            </TD>
            <TD>
              <para>Supported if the current user of the device is the same user who enrolled the device.</para>
            </TD>
          </tr>
          <tr>
            <TD>
              <para>Windows 8.1</para>
            </TD>
            <TD>
              <para>Supported if the current user of the device is the same user who enrolled the device.</para>
            </TD>
          </tr>
        </tbody>
      </table><procedure>
        <title>To lock a mobile device remotely through the Microsoft Intune console</title>
        <steps class="ordered">
          <step>
            <content>
              <para>In the <externalLink><linkText>Intune administrator  console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Groups</ui> &gt; <ui>All Devices</ui> &gt; <ui>All Mobile Devices</ui>.</para>
            </content>
          </step>
          <step>
            <content>
              <para>Click <ui>All Direct Managed Devices</ui> for devices enrolled in  Intune  or <ui>All Exchange ActiveSync Managed Devices</ui>.</para>
              <alert class="tip">
                <para>You can also navigate to a device by user. Click <ui>All Users</ui>. On the user's properties page, click <ui>Devices</ui>, and then click the name of the mobile device you want to wipe.</para>
              </alert>
            </content>
          </step>
          <step>
            <content>
              <para>In the list, click the device or devices that you want to lock. On the taskbar, click <ui>Remote Tasks</ui>, and select <ui>Remote Lock</ui>.</para>
            </content>
          </step>
        </steps>
      </procedure>
    </content>
            </section></sections>
  </section>
  
  
  <relatedTopics>
    <link xlink:href="3dbec400-5d8a-47be-b892-7745811d9de2">Retire data and devices from Microsoft Intune management</link>
    <externalLink>
      <linkText>Windows Selective Wipe for Device Data Management</linkText>
      <linkUri>http://technet.microsoft.com/library/dn486874.aspx</linkUri>
    </externalLink>
    
      
  </relatedTopics>
</developerHowToDocument>
