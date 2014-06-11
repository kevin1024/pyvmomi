vim.profile.host.HostProfile.CompleteConfigSpec
===============================================
inherits from [vim.profile.host.HostProfile.ConfigSpec](docs/vim.profile.host.HostProfile.ConfigSpec.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.host.HostProfile.CompleteConfigSpec.md">HostProfileCompleteConfigSpec</a> data object  specifies the complete configuration for a host profile.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| applyProfile | [vim.profile.host.HostApplyProfile](vim.profile.host.HostApplyProfile.md "vim.profile.host.HostApplyProfile") | true | None | Profile that contains configuration data for the host. |
| customComplyProfile | [vim.profile.ComplianceProfile](vim.profile.ComplianceProfile.md "vim.profile.ComplianceProfile") | true | None | User defined compliance profile.  Reserved for future use. |
| disabledExpressionListChanged | bool | None | None | Flag indicating if this configuration specification contains changes  in the <a href="vim.profile.host.HostProfile.CompleteConfigSpec.md#disabledExpressionList">disabledExpressionList</a>.  If False, the Profile Engine ignores the contents of the disabled expression list. |
| disabledExpressionList | string | true | None | List of expressions to be disabled. Each entry in the list specifies  a <a href="vim.profile.Expression.md">ProfileExpression</a>.<a href="vim.profile.Expression.md#id">id</a>.  All expressions are enabled by default.  <p>  If you set <a href="vim.profile.host.HostProfile.CompleteConfigSpec.md#disabledExpressionListChanged">disabledExpressionListChanged</a>  to True, the Profile Engine uses the contents of this list to replace the contents  of the <a href="vim.profile.host.HostProfile.md">HostProfile</a>.<a href="vim.profile.Profile.md#config">config</a>.<a href="vim.profile.host.HostProfile.ConfigInfo.md#disabledExpressionList">disabledExpressionList</a>.  <p>  The expression list is contained in the  <a href="vim.profile.host.HostProfile.ConfigInfo.md#defaultComplyProfile">defaultComplyProfile</a>.  The Profile Engine automatically generates the default compliance profile  when you create a host profile. |
| validatorHost | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | true | None | Host for profile validation. This can be a host on which the profile  is intended to be used. If you do not specify a validator host,  the Profile Engine uses the <a href="vim.profile.host.HostProfile.md">HostProfile</a>.<a href="vim.profile.host.HostProfile.md#referenceHost">referenceHost</a>  to validate the profile. |


