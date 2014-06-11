vim.profile.host.PortGroupProfile
=================================
inherits from [vim.profile.ApplyProfile](docs/vim.profile.ApplyProfile.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


<a href="vim.profile.host.PortGroupProfile.md">PortGroupProfile</a> is the base class for the different port group   subprofile objects.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Linkable identifier. |
| name | string | None | None | Name of the portgroup. |
| vlan | [vim.profile.host.PortGroupProfile.VlanProfile](vim.profile.host.PortGroupProfile.VlanProfile.md "vim.profile.host.PortGroupProfile.VlanProfile") | None | None | VLAN identifier for the port group. |
| vswitch | [vim.profile.host.PortGroupProfile.VirtualSwitchSelectionProfile](vim.profile.host.PortGroupProfile.VirtualSwitchSelectionProfile.md "vim.profile.host.PortGroupProfile.VirtualSwitchSelectionProfile") | None | None | Virtual switch to which the port group is connected. |
| networkPolicy | [vim.profile.host.NetworkPolicyProfile](vim.profile.host.NetworkPolicyProfile.md "vim.profile.host.NetworkPolicyProfile") | None | None | The network policy applicable on the port group. |


