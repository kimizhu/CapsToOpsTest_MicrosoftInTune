---
description: na
keywords: na
pagetitle: Network infrastructure requirements for Microsoft Intune
search: na
ms.date: 2015-11-17
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: get-started-article
ms.assetid: 074de65b-84a5-4a01-a824-18ffd838eab0
ms.author: f224bb9b442140c797af0e59b80f0d33
---
# Network infrastructure requirements for Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<developerWalkthroughDocument xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd">
  <introduction>
    <para>
        <token>wit_firstref</token> requires your network infrastructure to pass communications between the devices you manage and use to manage your subscription, and the websites on the Internet that the cloud-based service uses.</para>
      <para>There is no requirement to use on-premises infrastructure (like a server where you must install software), but there are options to use on-premises infrastructure including Exchange and Active Directory synchronization tools.</para>
    
    
  </introduction>
  <section address="BKMK_NetworkReqs">
        <title>Network infrastructure</title>
        <content>
          <para>To manage computers that are behind firewalls and proxy servers, you must set up firewalls and proxy servers to allow communications for <token>wit_nextref</token>.</para>
        </content>
        <sections>
          <section address="BKMK_FirewallReqs">
            <title>Requirements for firewalls, ports, and domains</title>
            <content>
              <para>Managed devices require configurations that let <ui>All Users</ui> access various services through firewalls.</para>
              <para>The following table lists the domains and services that the <token>wit_nextref</token> client accesses.</para>
              <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <legacyBold>Purpose</legacyBold>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <legacyBold>Domain</legacyBold>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <legacyBold>Ports</legacyBold>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD rowspan="13">
                      <para>Microsoft Intune and related services</para>
                    </TD>
                    <TD>
                      <para>*.manage.microsoft.com</para>
                    </TD>
                    <TD>
                      <para>80 and 443</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>*manage.microsoft.com</para>
                    </TD>
                    <TD>
                      <para>80 and 443</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>manage.microsoft.com</para>
                    </TD>
                    <TD>
                      <para>80 and 443</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>*.microsoftonline-p.com</para>
                    </TD>
                    <TD>
                      <para>80 and 443</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>*.microsoftonline-p.net</para>
                    </TD>
                    <TD>
                      <para>80 and 443</para>
                    </TD>
                  </tr><tr><TD><para>*.portal.office.com</para></TD><TD><para>80 and 443</para></TD></tr>
                  <tr>
                    <TD>
                      <para>*.spynet2.microsoft.com</para>
                    </TD>
                    <TD>
                      <para>443</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>c.microsoft.com</para>
                    </TD>
                    <TD>
                      <para>80 and 443</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>c1.microsoft.com</para>
                    </TD>
                    <TD>
                      <para>80 and 443</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>blob.core.windows.net</para>
                    </TD>
                    <TD>
                      <para>80 and 443</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <?Comment BD: 165602 2015-05-11T09:37:00Z  Id='9?>ajax.aspnetcdn.com<?CommentEnd Id='9'
    ?></para>
                    </TD>
                    <TD>
                      <para>80 and 443</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>*.googleapis.com<superscript>1</superscript></para>
                    </TD>
                    <TD>
                      <para>80 and 443</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>wustat.microsoft.com</para>
                    </TD>
                    <TD>
                      <para>80 and 443</para>
                    </TD>
                  </tr>
                  
                  <tr>
                    <TD rowspan="8">
                      <para>Microsoft Update Services</para>
                    </TD>
                    <TD>
                      <para>*.update.microsoft.com</para>
                    </TD>
                    <TD>
                      <para>80 and 443</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>download.microsoft.com</para>
                    </TD>
                    <TD>
                      <para>80 and 443</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>update.microsoft.com</para>
                    </TD>
                    <TD>
                      <para>80 and 443</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>*.download.windowsupdate.com</para>
                    </TD>
                    <TD>
                      <para>80 and 443</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>download.windowsupdate.com</para>
                    </TD>
                    <TD>
                      <para>80 and 443</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>*.windowsupdate.com</para>
                    </TD>
                    <TD>
                      <para>80 and 443</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>windowsupdate.microsoft.com</para>
                    </TD>
                    <TD>
                      <para>80 and 443</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>ntservicepack.microsoft.com</para>
                    </TD>
                    <TD>
                      <para>80 and 443</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>DNS lookup requests</para>
                    </TD>
                    <TD>
                      <para>manage.microsoft.com.nsatc.net</para>
                    </TD>
                    <TD>
                      <para>80</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>Samsung KNOX device communication through the firewall </para>
                    </TD>
                    <TD colspan="2">
                      <para>To enable Samsung KNOX devices to contact KNOX servers through the firewall, follow the instructions on the <externalLink><linkText>Samsung KNOX FAQ</linkText><linkUri>https://www.samsungknox.com/en/faq/our-corporate-devices-are-behind-firewall-how-do-i-enable-knox-devices-contact-samsung-servers</linkUri></externalLink>.</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD rowspan="7">
                      <para>Documentation, Help, and support</para>
                    </TD>
                    <TD>
                      <para>*.livemeeting.com</para>
                    </TD>
                    <TD>
                      <para>80 and 443</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>*.microsoftonline.com</para>
                    </TD>
                    <TD>
                      <para>80 and 443</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>*.social.technet.microsoft.com</para>
                    </TD>
                    <TD>
                      <para>80</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>blogs.technet.com</para>
                    </TD>
                    <TD>
                      <para>80</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>go.microsoft.com</para>
                    </TD>
                    <TD>
                      <para>80</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>onlinehelp.microsoft.com</para>
                    </TD>
                    <TD>
                      <para>80</para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>www.microsoft.com</para>
                    </TD>
                    <TD>
                      <para>80</para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <superscript>1</superscript> This domain is required for JQuery support when you use the company portal website.</para>
            </content>
          </section>
          <section address="BKMK_ProxyReqs">
            <title>Requirements for proxy servers </title>
            <content>
              <para>To manage computers that are behind a proxy server, consider the following:</para>
              <list class="bullet">
                <listItem>
                  <para>The proxy server must support both <embeddedLabel>HTTP</embeddedLabel> and <embeddedLabel>HTTPS</embeddedLabel> because <token>wit_nextref</token> clients use both protocols.</para>
                </listItem>
                <listItem>
                  <para>
                    <token>wit_nextref</token> supports unauthenticated proxy servers.</para>
                </listItem>
              </list>
              <para>You can modify proxy server settings on individual client computers, or you can use Group Policy settings to change settings for all client computers that are located behind a specified proxy server.</para>
              <para>You can also use a proxy server that caches content to <externalLink><linkText>reduce network bandwidth</linkText><linkUri>http://technet.microsoft.com/library/dn646966.aspx#BKMK_reduceBandwidth</linkUri></externalLink> use by <token>wit_nextref</token> clients.</para>
            </content>
          </section>
        </sections>
      </section><section address="BKMK_OnPremisesReqs">
        <title>On-premises infrastructure</title>
        <content>
          <para>The following table identifies on-premises infrastructure you can use with <token>wit_firstref</token>.</para>
          <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
            <thead>
              <tr>
                <TD>
                  <para>Infrastructure</para>
                </TD>
                <TD>
                  <para>More information</para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>On-Premises Connector</para>
                </TD>
                <TD>
                  <para>Use the <embeddedLabel>On-Premises Connector</embeddedLabel> to synchronize data from Exchange Server:</para>
                  <list class="bullet">
                    <listItem>
                      <para>If your instance of Exchange Server is on-premises, you must download, install, and <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac#bkmk_EX_OP">set up the Microsoft Intune On-Premises Connector</link> on a computer in your infrastructure. This connector can also connect to Exchange in the cloud.</para>
                    </listItem>
                    <listItem>
                      <para>If your instance of Exchange Server is hosted in a cloud-based service, you can install and configure the On-Premises Connector, or you can <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac#bkmk_S_S">configure the built-in Microsoft Intune Service to Service Connector</link> which does not require an on-premises server to host the connector.</para>
                    </listItem>
                  </list>
                  <para>Before you can use either connector to connect <token>wit_nextref</token> to your Exchange Server, you must <externalLink><linkText>set up Active Directory synchronization</linkText><linkUri>http://technet.microsoft.com/library/dn646983.aspx#BKMK_SyncUsersFromAD</linkUri></externalLink> so that your local users and security groups are synchronized with your instance of Azure AD. </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>Proxy server</para>
                </TD>
                <TD>
                  <para>If you manage clients that access the Internet through a proxy server, see <link xlink:href="074de65b-84a5-4a01-a824-18ffd838eab0#BKMK_ProxyReqs">Requirements for proxy servers</link>.</para>
                  <para>You can also use a proxy server that caches content to reduce network bandwidth. For more information, see <link xlink:href="5d1ac59c-a885-4276-8576-f3cf81c2d268#BKMK_ReduceBandwidth">Reduce network bandwidth use</link> in the <link xlink:href="5d1ac59c-a885-4276-8576-f3cf81c2d268">What to know before setting up Microsoft Intune</link> topic. </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
        <sections>
          <section address="BKMK_ExchanceConnectorReqs">
            <title>Requirements for the On-Premises Connector</title>
            <content>
              <para>The following table lists the requirements for the computer where you install the On-Premises Connector.</para>
              <table xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
                <thead>
                  <tr>
                    <TD>
                      <para>Requirement</para>
                    </TD>
                    <TD>
                      <para>More information</para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>Operating systems</para>
                    </TD>
                    <TD>
                      <para>
                        <token>wit_nextref</token> supports the On-Premises Connector on a computer that runs any edition of the following operating systems: </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <token>longhornshort</token> SP2 64 bit</para>
                        </listItem>
                        <listItem>
                          <para>
                            <token>nextref_server_7</token>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <token>win8_server_2</token>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <token>winblue_server_2</token>
                          </para>
                        </listItem>
                      </list>
                      <alert class="note">
                        <para>The connector is not supported on any Server Core installation.</para>
                      </alert>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>Microsoft Exchange version</para>
                    </TD>
                    <TD>
                      <para>
                        <?Comment RS: Requested by Jon Lynn 2015-03-03T13:43:00Z  Id='85?>The On-Premises Connector requires Microsoft Exchange 2010 SP1 or later.<?CommentEnd Id='85'
    ?></para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>Hardware</para>
                    </TD>
                    <TD>
                      <para>The computer where you install the connector requires the following minimum hardware: </para>
                      <list class="bullet">
                        <listItem>
                          <para>1.6 GHz CPU</para>
                        </listItem>
                        <listItem>
                          <para>2 GB ram</para>
                        </listItem>
                        <listItem>
                          <para>10 GB of free disk space</para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>Additional software</para>
                    </TD>
                    <TD>
                      <para>The following must be installed on the computer that hosts the connector:</para>
                      <list class="bullet">
                        <listItem>
                          <para>Full installation of Microsoft .NET Framework 4</para>
                        </listItem>
                        <listItem>
                          <para>At a minimum, <token>wps_2</token> 2.0</para>
                        </listItem>
                      </list>
                      <alert class="note">
                        <para>The connector is not supported on a computer that runs an Exchange Server role.</para>
                      </alert>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>Network</para>
                    </TD>
                    <TD>
                      <para>The computer where you install the connector must be in a domain that has a trust relationship to the domain that hosts your Exchange Server.</para>
                      <para/>
                      <para>The computer requires configurations to enable it to access the <token>wit_nextref</token> service through firewalls and proxy servers over Ports 80 and 443. Domains used by <token>wit_nextref</token> include:</para>
                      <list class="bullet">
                        <listItem>
                          <para>manage.microsoft.com</para>
                        </listItem>
                        <listItem>
                          <para>*manage.microsoft.com</para>
                        </listItem>
                        <listItem>
                          <para>*.manage.microsoft.com</para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_ServiceConnectorReqs">
            <title>Requirements for the Service to Service Connector</title>
            <content>
              <para>The Service to Service Connector supports only cloud-based Exchange and has no requirements for on-premises infrastructure.</para>
              <para>However, to use this connector, the following must be true:</para>
              <list class="bullet">
                <listItem>
                  <para>You have an Office 365 subscription that has an Exchange Server 2013 tenant. So long as the tenant is Exchange Server 2013, the connector supports Exchange Server 2010 in that same environment.</para>
                </listItem>
                <listItem>
                  <para>The user account that you use to install the On-Premises Connector must be a tenant administrator for <token>wit_nextref</token> and be an administrator in the Exchange tenant with a license to use Exchange Server 2013.</para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
  
  
  <relatedTopics>
    <link xlink:href="5d1ac59c-a885-4276-8576-f3cf81c2d268">What to know before setting up Microsoft Intune</link><externalLink>
      <linkText>How to buy Intune</linkText>
      <linkUri>http://technet.microsoft.com/library/dn646949.aspx</linkUri>
    </externalLink>
  </relatedTopics>
</developerWalkthroughDocument>
