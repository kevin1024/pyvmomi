vim.profile.host.HostProfile
============================
inherits from [vim.profile.Profile](vim.profile.Profile.md "vim.profile.Profile")
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


A host profile describes ESX Server configuration.   The <a href="vim.profile.host.HostProfile.md">HostProfile</a> managed object provides access to profile data and   it defines methods to manipulate the profile.   A host profile is a combination of subprofiles, each of which contains   configuration data for a specific capability. Some examples of host capabilities are   authentication, memory, networking, and security. For access to individual subprofiles,   see the <a href="vim.profile.host.HostApplyProfile.md">HostApplyProfile</a> data object   (<a href="vim.profile.host.HostProfile.md">HostProfile</a>.<a href="vim.profile.Profile.md#config">config</a>.<a href="vim.profile.host.HostProfile.ConfigInfo.md#applyProfile">applyProfile</a>).   <p>   Host profiles are part of the stateless configuration architecture.   In the stateless environment, a Profile Engine runs on each ESX host,   but an ESX host does not store its own configuration state. Instead,   host configuration data is stored on vCenter Servers. Every time a host   boots or reboots, it obtains its profile from the vCenter Server.   <ul>   <li>To create a base host profile use the   <a href="vim.profile.host.ProfileManager.md">HostProfileManager</a>.<a href="vim.profile.ProfileManager.md#createProfile">CreateProfile</a>   method. To create a profile from an ESX host, specify a   <a href="vim.profile.host.HostProfile.HostBasedConfigSpec.md">HostProfileHostBasedConfigSpec</a>. To create a profile from a file,   specify a <a href="vim.profile.host.HostProfile.SerializedHostProfileSpec.md">HostProfileSerializedHostProfileSpec</a>.<br/><br/>   </li>   <li>To create a subprofile for a particular host capability, use the   <a href="vim.profile.host.ProfileManager.md">HostProfileManager</a>.<a href="vim.profile.host.ProfileManager.md#createDefaultProfile">CreateDefaultProfile</a>   method. After you create the default profile you can modify it and save it in the base profile.   <br/><br/>   </li>   <li>To update an existing profile, use the   <a href="vim.profile.host.HostProfile.md">HostProfile</a>.<a href="vim.profile.host.HostProfile.md#update">UpdateHostProfile</a> method.<br/><br/>   </li>   <li>   To apply a host profile to an ESX host, use the <a href="vim.profile.host.HostProfile.md#execute">ExecuteHostProfile</a> method   to generate configuration changes, then call the   <a href="vim.profile.host.ProfileManager.md">HostProfileManager</a>.<a href="vim.profile.host.ProfileManager.md#applyHostConfiguration">ApplyHostConfig_Task</a>   method to apply them.   </li>   </ul>   <p>   <u>Host-Specific Configuration</u>   <p>   An individual host or a set of hosts may have some configuration settings   that are different from the settings specified in the host profile.   For example, the IP configuration for the host's virtual network adapters   must be unique.   <ul>   <li>To verify host-specific data, use the <code>deferredParam</code> parameter   to the <a href="vim.profile.host.HostProfile.md#execute">ExecuteHostProfile</a> method.   The Profile Engine will determine if you have specified all of the required   parameters for the host configuration. If additional data is required,   call the <a href="vim.profile.host.HostProfile.md#execute">ExecuteHostProfile</a> method again as many times as necessary   to verify a complete set of parameters.   <br/><br/>   </li>   <li>To apply host-specific data, use the <code>userInput</code> parameter to the   <a href="vim.profile.host.ProfileManager.md">HostProfileManager</a>.<a href="vim.profile.host.ProfileManager.md#applyHostConfiguration">ApplyHostConfig_Task</a>    method.   <br/><br/>   </li>   </ul>   The Profile Engine saves host-specific data in an <a href="vim.profile.host.AnswerFile.md">AnswerFile</a>   that is stored on the vCenter Server.   The <a href="vim.profile.host.ProfileManager.md">HostProfileManager</a> provides several methods to manipulate   answer files.   <p>   <u>Profile Compliance</u>   <p>   You can create associations between hosts and profiles to support compliance checking.   When you perform compliance checking, you can determine if a host configuration   conforms to a host profile.   <ul>   <li>To create an association between a host and a profile, use the   <a href="vim.profile.Profile.md#associateEntities">AssociateProfile</a> method.   The method adds the host to the   <a href="vim.profile.host.HostProfile.md">HostProfile</a>.<a href="vim.profile.Profile.md#entity">entity</a>[] list.   <br/><br/></li>   <li>To retrieve the list of profiles associated with a host, use the   <a href="vim.profile.host.ProfileManager.md">HostProfileManager</a>.<a href="vim.profile.ProfileManager.md#findAssociatedProfile">FindAssociatedProfile</a>   method.   <br/><br/></li>   <li>To check host compliance, use the   <a href="vim.profile.Profile.md#checkCompliance">CheckProfileCompliance_Task</a> method.   If you do not specify any hosts, the method will check the compliance of all hosts   that are associated with the profile.   <br/><br/></li>   </ul>   You can also use the Profile Compliance Manager to check compliance by specifying   profiles, entities (hosts), or both. See   <a href="vim.profile.ComplianceManager.md">ProfileComplianceManager</a>.<a href="vim.profile.ComplianceManager.md#checkCompliance">CheckCompliance_Task</a>.   <p>   <u>Profile Plug-Ins</u>   <p>   The vSphere architecture uses VMware profile plug-ins to define profile extensions.   For information about using a plug-in to extend a host profile, see the VMware Technical Note   <i>Developing a Host Profile Extension Plug-in</i>.   <p>   For access to host configuration data that is defined by plug-ins, use the   <a href="vim.profile.ApplyProfile.md">ApplyProfile</a>.<a href="vim.profile.ApplyProfile.md#policy">policy</a>[] and   <a href="vim.profile.ApplyProfile.md">ApplyProfile</a>.<a href="vim.profile.ApplyProfile.md#property">property</a>[] lists.   The <a href="vim.profile.host.HostApplyProfile.md">HostApplyProfile</a> and its subprofiles, which collectively   define host configuration data, are derived from the <a href="vim.profile.ApplyProfile.md">ApplyProfile</a>.   <ul>   <li>Policies store ESX configuration data in <a href="vim.profile.PolicyOption.md">PolicyOption</a> objects.</li>   <li>Profile property lists contain subprofiles defined by plug-ins. Subprofiles can be nested.   <ul>   <li>Subprofile lists are available as an extension to the base host profile   (<a href="vim.profile.host.HostProfile.md">HostProfile</a>.<a href="vim.profile.Profile.md#config">config</a>.<a href="vim.profile.host.HostProfile.ConfigInfo.md#applyProfile">applyProfile</a>.<a href="vim.profile.ApplyProfile.md#property">property</a>[]).   </li>   <li>Subprofile lists are available as extensions to the host subprofiles - for example,     the network subprofile   (<a href="vim.profile.host.HostApplyProfile.md">HostApplyProfile</a>.<a href="vim.profile.host.HostApplyProfile.md#network">network</a>.<a href="vim.profile.ApplyProfile.md#property">property</a>[]).   </li>   </ul>   </li>   </ul>   <br/>   If you make changes to host profile data, later versions of profile plug-ins may not support   the host configuration implied by the changes that you make. When a subsequent vSphere   version becomes available, you must verify that the new version supports any previous   configuration changes that you have made.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='referenceHost'>referenceHost</a> | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | true | None | Reference host in use for this host profile. To set this property,  use the <a href="vim.profile.host.HostProfile.md#updateReferenceHost">UpdateReferenceHost</a>  method. If you do not specify a host for validation  (<a href="vim.profile.host.HostProfile.CompleteConfigSpec.md">HostProfileCompleteConfigSpec</a>.<a href="vim.profile.host.HostProfile.CompleteConfigSpec.md#validatorHost">validatorHost</a>),  the Profile Engine uses the reference host to validate the profile. |


UpdateReferenceHost([host](vim.HostSystem.md "vim.HostSystem"))
---------------------------------------------------------------

| service name | UpdateReferenceHost |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | Profile.Edit |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




UpdateHostProfile([config](vim.profile.host.HostProfile.ConfigSpec.md "vim.profile.host.HostProfile.ConfigSpec"))
-----------------------------------------------------------------------------------------------------------------
 raises [vim.fault.ProfileUpdateFailed](vim.fault.ProfileUpdateFailed.md "vim.fault.ProfileUpdateFailed"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName")

---
| service name | UpdateHostProfile |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | Profile.Edit |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | If the profile with the new name already exists. |
| [vim.fault.ProfileUpdateFailed](vim.fault.ProfileUpdateFailed.md "vim.fault.ProfileUpdateFailed") | if errors were encountered when updating     the profile. |




ExecuteHostProfile([host](vim.HostSystem.md "vim.HostSystem"), [deferredParam](vim.profile.DeferredPolicyOptionParameter.md "vim.profile.DeferredPolicyOptionParameter"))
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

| service name | ExecuteHostProfile |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




