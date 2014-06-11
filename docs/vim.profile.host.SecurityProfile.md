vim.profile.host.SecurityProfile
================================
inherits from [vim.profile.ApplyProfile](docs/vim.profile.ApplyProfile.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.host.SecurityProfile.md">SecurityProfile</a> data object represents host security configuration.  If a profile plug-in defines policies or subprofiles, use the  <a href="vim.profile.ApplyProfile.md#policy">policy</a> or <a href="vim.profile.ApplyProfile.md#property">property</a>  list to access the additional configuration data.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| permission | [vim.profile.host.PermissionProfile](vim.profile.host.PermissionProfile.md "vim.profile.host.PermissionProfile") | true | None | Permission configuration. |


