vim.profile.host.VirtualSwitchProfile
=====================================
inherits from [vim.profile.ApplyProfile](docs/vim.profile.ApplyProfile.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.host.VirtualSwitchProfile.md">VirtualSwitchProfile</a> data object represents a subprofile   for a virtual switch. If a profile plug-in defines policies or subprofiles, use the  <a href="vim.profile.ApplyProfile.md#policy">policy</a> or <a href="vim.profile.ApplyProfile.md#property">property</a>  list to access the additional configuration data.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Linkable identifier. |
| name | string | None | None | Name of the virtual switch. |
| link | [vim.profile.host.VirtualSwitchProfile.LinkProfile](vim.profile.host.VirtualSwitchProfile.LinkProfile.md "vim.profile.host.VirtualSwitchProfile.LinkProfile") | None | None | Links that are connected to the virtual switch. |
| numPorts | [vim.profile.host.VirtualSwitchProfile.NumPortsProfile](vim.profile.host.VirtualSwitchProfile.NumPortsProfile.md "vim.profile.host.VirtualSwitchProfile.NumPortsProfile") | None | None | Number of ports on the virtual switch. |
| networkPolicy | [vim.profile.host.NetworkPolicyProfile](vim.profile.host.NetworkPolicyProfile.md "vim.profile.host.NetworkPolicyProfile") | None | None | Network policy for the virtual switch. |


