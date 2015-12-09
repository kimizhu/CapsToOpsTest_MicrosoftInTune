This topic provide specific recommendations for a phased rollout of policies in [!INC[wit_firstref](../Token/wit_firstref_md.md)]. This approach applies to the first policies you apply in a new [!INC[wit_nextref](../Token/wit_nextref_md.md)] deployment, or policies you add to an existing deployment.

For general information about rollout phases, see [Rollout phases for Microsoft Intune deployment](../Topic/Rollout_phases_for_Microsoft_Intune_deployment.md).

## Phases of policy rollout
The phases of policy rollout are:

- Project scope

- Proof of concept

- Pilot

- Enterprise rollout

- Run state

### Project scope
Define the scope of your [!INC[wit_nextref](../Token/wit_nextref_md.md)] policy deployment:

- For a new implementation, this will require defining all of the desired device behaviors and security requirements that you want to create with your policy set.

- Decide what users and devices  you want to impact with these policies.

- Design your user and device groups to enable you to apply the new policies appropriately.

- Determine whether  there are limitations or requirements associated with each operating system that will affect the intentions of your policy.

- Consider policy design specifics, such as policy type and template to be used.

- Whether you are launching your first set of policies or adding new policies to an existing policy set, consider how various policies interact, and what the likely device behavior will be. Issues with policy interactions and conflicts can be discovered in the Pilot phase, but catching policy conflicts in early planning will simplify execution of the Pilot.

### Proof of concept
In the Proof of concept phase, test your policy deployment in a laboratory environment on devices and users that you've configured strictly for testing purposes.

- Have your help desk participate in this phase to learn what issues can arise during pilot and production deployment.  Troubleshooting information is available in [Troubleshoot policies in Microsoft Intune](http://msdn.microsoft.com/en-us/library/d56fa548-8297-4a22-979c-157f6d7834e6).

- At this point in the process you should develop communication plans for pilot and production users. At a minimum the plan should include  what device behaviors will change and when, and the business purpose for the change, and what to do if they encounter issues, both self-help information and how to contact the help desk.

### Pilot
During the pilot you will deploy the policy to a small group of test users and devices. There are specific considerations for piloting policy in [!INC[wit_nextref](../Token/wit_nextref_md.md)]:

- The test  group should be representative of the group to which the policy will be applied for production rollout.

- Educate the help desk  regarding the changes in policy, and ensure they are prepared to help users in the test group.

- Activate your pilot user communication plan.

- The pilot can first be done in isolated mode, where the device is not subject to other policies that may cause conflict and unintended behavior.

- The final test must consider the new policy and all the existing policies that will be applied to the same device.

### Enterprise rollout

- Based on the results of the pilot, adjust your planned policy to correct for policy conflicts and unanticipated behavior.

- Notify your help desk of the enterprise rollout schedule. Have mechanisms in place to respond to help requests, and to adjust the rollout as necessary.

- Be prepared to troubleshoot the policy if issues arise.

- Activate your production user communication plan.

- Apply the policies incrementally to additional groups, monitoring the policy state for affected devices and tracking help desk requests that may be related to the new policy.

### Run state
**Operations:** Monitor your [!INC[wit_nextref](../Token/wit_nextref_md.md)] console for alerts and user or device issues, and to ensure that polices are performing according to your organizational plan.

**Help desk:** Ensure that your help desk is aware of any changes to policies that will affect the user experience, as these may result in support requests.

## See Also
[Troubleshoot policies in Microsoft Intune](http://msdn.microsoft.com/en-us/library/d56fa548-8297-4a22-979c-157f6d7834e6)
[Use policies to manage computers and mobile devices with Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

