vim.profile.host.HostProfile.ConfigInfo
=======================================
inherits from [vim.profile.Profile.ConfigInfo](docs/vim.profile.Profile.ConfigInfo.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.host.HostProfile.ConfigInfo.md">HostProfileConfigInfo</a> data object  contains host profile data and information about profile compliance.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| applyProfile | [vim.profile.host.HostApplyProfile](vim.profile.host.HostApplyProfile.md "vim.profile.host.HostApplyProfile") | true | None | Profile data for host configuration. |
| defaultComplyProfile | [vim.profile.ComplianceProfile](vim.profile.ComplianceProfile.md "vim.profile.ComplianceProfile") | true | None | Default compliance profile. The ESX Server uses the <code>applyProfile</code>  (<a href="vim.profile.host.HostProfile.md">HostProfile</a>.<a href="vim.profile.Profile.md#config">config</a>.<a href="vim.profile.host.HostProfile.ConfigInfo.md#applyProfile">applyProfile</a>)  to generate the default compliance profile when you create a host profile.  When the <code>applyProfile</code> is modified, the Server automatically  updates the compliance profile to match it. |
| defaultComplyLocator | [vim.profile.ComplianceLocator](vim.profile.ComplianceLocator.md "vim.profile.ComplianceLocator") | true | None | List of compliance locators. Each locator specifies an association between  the <code>applyProfile</code> and the <code>defaultComplyProfile</code>.  The association identifies a component profile and the expression generated  by the profile. vSphere clients can use this data to provide contextual  information to the user. |
| customComplyProfile | [vim.profile.ComplianceProfile](vim.profile.ComplianceProfile.md "vim.profile.ComplianceProfile") | true | None | User defined compliance profile.  Reserved for future use. |
| disabledExpressionList | string | true | None | Disabled expressions in the default compliance profile  (<code>DefaultComplyProfile</code>).  Use this property to specify which expressions are disabled.  All expressions are enabled by default. |


