vim.dvs.HostMember
==================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.dvs.HostMember.md">DistributedVirtualSwitchHostMember</a> data object represents an ESXi host that   is a member of a distributed virtual switch. When you add a host to a switch   (<a href="vim.dvs.HostMember.ConfigSpec.md">DistributedVirtualSwitchHostMemberConfigSpec</a>.<a href="vim.dvs.HostMember.ConfigSpec.md#host">host</a>),   the Server creates a proxy switch (<a href="vim.host.HostProxySwitch.md">HostProxySwitch</a>).   The host member object contains information about the configuration   and state of the proxy.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| runtimeState | [vim.dvs.HostMember.RuntimeState](vim.dvs.HostMember.RuntimeState.md "vim.dvs.HostMember.RuntimeState") | true | None | Host member runtime state. |
| config | [vim.dvs.HostMember.ConfigInfo](vim.dvs.HostMember.ConfigInfo.md "vim.dvs.HostMember.ConfigInfo") | None | None | Host member configuration. |
| productInfo | [vim.dvs.ProductSpec](vim.dvs.ProductSpec.md "vim.dvs.ProductSpec") | true | None | Vendor, product and version information for the proxy switch   module. |
| uplinkPortKey | string | true | None | Port keys of the uplink ports created for the host member. These ports   will be deleted after the host leaves the switch. |
| status | string | None | None | The host DistributedVirtualSwitch component status. See   <a href="vim.dvs.HostMember.HostComponentState.md">HostComponentState</a> for valid values. |
| statusDetail | string | true | None | Additional information regarding the host's current status. |


