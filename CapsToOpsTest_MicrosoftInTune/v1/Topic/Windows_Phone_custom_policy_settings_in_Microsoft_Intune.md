Use the [!INC[wit_firstref](../Token/wit_firstref_md.md)]**Windows Phone custom configuration policy** to deploy OMA-URI (Open Mobile Alliance Uniform Resource Identifier) settings that can be used to control features on **Windows Phone 8.1 devices**. These are standard settings that many mobile device manufacturers use to control device features.

This capability is intended to allow you to deploy Windows Phone settings that are not configurable with an [!INC[wit_nextref](../Token/wit_nextref_md.md)] policy. For information about the settings you can configure with these policies, see [Manage settings and features on your devices with Microsoft Intune policies](../Topic/Manage_settings_and_features_on_your_devices_with_Microsoft_Intune_policies.md).

For help creating OMA-URI settings for Windows Phone devices, see [Windows Phone 8.1 MDM protocol documentation](http://technet.microsoft.com/library/dn499787.aspx).

## How to create a Windows Phone custom policy

1. In the [Microsoft Intune administration console](https://manage.microsoft.com), click **Policy** &gt; **Add Policy**.

2. Under **Windows**, configure a **Custom Configuration (Windows Phone 8.1 and later)** policy.

   For help creating and deploying policies, see the [Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

   You can only create and deploy a custom policy. Recommended settings are not available.

3. Use the following table to help you configure the general policy settings:

   |Setting name <br /> <br />|More information <br /> <br />|
   |----------------|--------------------|
   |**Name** <br /> <br />|Enter a unique name for the policy to help you identify it in the [!INC[wit_nextref](../Token/wit_nextref_md.md)] console. <br /> <br />|
   |**Description** <br /> <br />|Provide a description that gives an overview of the policy and other relevant information that helps you to locate it. <br /> <br />|

4. In the **OMA-URI Settings** section, click **Add** to add a setting. You can also edit or delete an existing setting.

5. In the **Add or Edit OMA-URI** Setting dialog box, specify the following information:

   |Item <br /> <br />|More information <br /> <br />|
   |--------|--------------------|
   |**Setting name** <br /> <br />|Enter a unique name for the OMA-URI setting to help you identify it in the list of settings. <br /> <br />|
   |**Setting description** <br /> <br />|Provide a description that gives an overview of the setting and other relevant information to help you locate it. <br /> <br />|
   |**Data type** <br /> <br />|Select the date type in which you will specify this OMA-URI setting. Choose from: <br /> <br /><ul><li>**String** </li><li>**String (XML)** </li><li>**Date and time** </li><li>**Integer** </li><li>**Floating point** </li><li>**Boolean** </li> </ul>|
   |**OMA-URI (Case Sensitive)** <br /> <br />|Specify the OMA-URI you want to supply a setting for. <br /> <br />|
   |**Value** <br /> <br />|Specify the value to associate with the OMA-URI you specified previously. <br /> <br />|

6. Click **OK** to save the setting and return to the **Create Policy** page.

7. Continue to add as many settings as you require. When you are done, click **Save Policy**.

The new policy displays in the **Configuration Policies** node of the **Policy** workspace.

## Deploy a Windows Phone Custom policy

1. Deploy the policy to one or more groups of users or devices in your organization.

For more information about how to deploy policies, see [Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

A status summary and alerts on the **Overview** page of the **Policy** workspace identify issues with the policy that require your attention. Additionally, a status summary appears in the **Dashboard** workspace.

## See Also
[Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

