vim.profile.host.AuthenticationProfile
======================================
inherits from [vim.profile.ApplyProfile](docs/vim.profile.ApplyProfile.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


The <a href="vim.profile.host.AuthenticationProfile.md">AuthenticationProfile</a> data object represents the host configuration  for authentication. If a profile plug-in defines policies or subprofiles, use the  <a href="vim.profile.ApplyProfile.md#policy">policy</a> or <a href="vim.profile.ApplyProfile.md#property">property</a>  list to access the additional configuration data.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| activeDirectory | [vim.profile.host.ActiveDirectoryProfile](vim.profile.host.ActiveDirectoryProfile.md "vim.profile.host.ActiveDirectoryProfile") | true | None | Subprofile representing the Active Directory configuration. |


