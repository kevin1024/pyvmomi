vim.dvs.HostMember.ConfigInfo
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.dvs.HostMember.ConfigInfo.md">DistributedVirtualSwitchHostMemberConfigInfo</a> data object  contains membership configuration information for the ESXi host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| host | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | true | None | ESXi host.  This property should always be set unless the user's setting  does not have System.Read privilege on the object referred to  by this property. |
| maxProxySwitchPorts | int | None | None | Maximum number of ports than can be created in the proxy switch.  <p>  <i>ESXi 5.0 and earlier hosts</i>:  If you change the maximum number of ports, you must reboot  the host for the new value to take effect. |
| vendorSpecificConfig | [vim.dvs.KeyedOpaqueBlob](vim.dvs.KeyedOpaqueBlob.md "vim.dvs.KeyedOpaqueBlob") | true | None | Opaque binary blob that stores vendor specific configuration. |
| backing | [vim.dvs.HostMember.Backing](vim.dvs.HostMember.Backing.md "vim.dvs.HostMember.Backing") | None | None | Host membership backing, specifying physical NIC, portgroup, and port  bindings for the proxy switch. |


