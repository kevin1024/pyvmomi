vim.host.PhysicalNic.NetworkHint
================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The NetworkHint data object type is some information about    the network to which the    physical network adapter is attached.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| device | string | None | None | The physical network adapter device to which    this hint applies. |
| subnet | [vim.host.PhysicalNic.NetworkHint.IpNetwork](vim.host.PhysicalNic.NetworkHint.IpNetwork.md "vim.host.PhysicalNic.NetworkHint.IpNetwork") | true | None | The list of subnets that were detected on this    physical network adapter. |
| network | [vim.host.PhysicalNic.NetworkHint.NamedNetwork](vim.host.PhysicalNic.NetworkHint.NamedNetwork.md "vim.host.PhysicalNic.NetworkHint.NamedNetwork") | true | None | The list of network names that were detected on this    physical network adapter. |
| connectedSwitchPort | [vim.host.PhysicalNic.CdpInfo](vim.host.PhysicalNic.CdpInfo.md "vim.host.PhysicalNic.CdpInfo") | true | None | If the uplink directly connects to a CDP-awared network device    and the device's CDP broadcast is enabled, this property will be    set to return the CDP information that vmkernel received on this    Physical NIC. CDP data contains the device information and port ID that    the Physical NIC connects to. If the uplink is not connecting to a    CDP-awared device or CDP is not enabled on the device, this    property will be unset.   <a href="vim.host.PhysicalNic.CdpInfo.md">PhysicalNicCdpInfo</a> |
| lldpInfo | [vim.host.PhysicalNic.LldpInfo](vim.host.PhysicalNic.LldpInfo.md "vim.host.PhysicalNic.LldpInfo") | true | None | If the uplink directly connects to an LLDP-aware network device and   the device's LLDP broadcast is enabled, this property will be set to   return the LLDP information that is received on this physical network   adapter. If the uplink is not connecting to a LLDP-aware device or   LLDP is not enabled on the device, this property will be unset. |


