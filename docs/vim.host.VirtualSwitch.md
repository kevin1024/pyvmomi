vim.host.VirtualSwitch
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The virtual switch is a software entity to which multiple virtual network   adapters can connect to create a virtual network.  It can also be   bridged to a physical network.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | The name of the virtual switch.   Maximum length is 32 characters. |
| key | string | None | None | The virtual switch key. |
| numPorts | int | None | None | The number of ports that this virtual switch currently has. |
| numPortsAvailable | int | None | None | The number of ports that are available on this virtual switch.  There   are a number of networking services that utilize a port on the virtual   switch and are not accounted for in the Port array of a PortGroup.  For   example, each physical NIC attached to a virtual switch consumes one   port.  This property should be used when attempting to implement   admission control for new services attaching to virtual switches. |
| mtu | int | true | None | The maximum transmission unit (MTU) associated with this virtual switch   in bytes. |
| portgroup | [vim.host.PortGroup](vim.host.PortGroup.md "vim.host.PortGroup") | true | None | The list of port groups configured for this virtual switch. |
| pnic | [vim.host.PhysicalNic](vim.host.PhysicalNic.md "vim.host.PhysicalNic") | true | None | The set of physical network adapters associated with this bridge. |
| spec | [vim.host.VirtualSwitch.Specification](vim.host.VirtualSwitch.Specification.md "vim.host.VirtualSwitch.Specification") | None | None | The specification of a PortGroup. |


