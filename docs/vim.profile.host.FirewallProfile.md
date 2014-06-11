vim.profile.host.FirewallProfile
================================
inherits from [vim.profile.ApplyProfile](docs/vim.profile.ApplyProfile.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.host.FirewallProfile.md">FirewallProfile</a> data object represents a host firewall configuration.  If a profile plug-in defines policies or subprofiles, use the  <a href="vim.profile.ApplyProfile.md#policy">policy</a> or <a href="vim.profile.ApplyProfile.md#property">property</a>  list to access the additional configuration data.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ruleset | [vim.profile.host.FirewallProfile.RulesetProfile](vim.profile.host.FirewallProfile.RulesetProfile.md "vim.profile.host.FirewallProfile.RulesetProfile") | true | None | List of Rulesets that will be configured for the firewall subprofile. |


