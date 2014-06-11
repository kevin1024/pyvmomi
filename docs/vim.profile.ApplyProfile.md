vim.profile.ApplyProfile
========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.ApplyProfile.md">ApplyProfile</a> data object is the base class for all data objects   that define profile configuration data.   <code>ApplyProfile</code> defines ESX configuration data storage and it   supports recursive profile definition for the profile plug-in architecture.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| enabled | bool | None | None | Indicates whether the profile is enabled. |
| policy | [vim.profile.Policy](vim.profile.Policy.md "vim.profile.Policy") | true | None | The list of policies comprising the profile. A <a href="vim.profile.Policy.md">ProfilePolicy</a>  stores one or more configuration data values in a <a href="vim.profile.PolicyOption.md">PolicyOption</a>.  The policy option is one of the configuration options from the  <a href="vim.profile.PolicyMetadata.md">ProfilePolicyMetadata</a>.<a href="vim.profile.PolicyMetadata.md#possibleOption">possibleOption</a>  list. |
| profileTypeName | string | true | None | Identifies the profile type. |
| profileVersion | string | true | None | Profile engine version. |
| property | [vim.profile.ApplyProfileProperty](vim.profile.ApplyProfileProperty.md "vim.profile.ApplyProfileProperty") | true | None | List of subprofiles for this profile.  This list can change depending on which profile plug-ins are available in the system.  Subprofiles can be nested to arbitrary depths to represent host capabilities. |


