vim.host.VirtualNic
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The <a href="vim.host.VirtualNic.md">HostVirtualNic</a> data object describes a virtual network adapter representing    an adapter that connects to a virtual switch. A host virtual NIC differs from a   physical NIC:   <ul>   <li>A host virtual NIC is a virtual device that is connected to a virtual switch.   <li>A physical NIC (<a href="vim.host.NetworkInfo.md">HostNetworkInfo</a>.<a href="vim.host.NetworkInfo.md#pnic">pnic</a>)   corresponds to a physical device that is connected to the physical network.   </ul>   <p>   A host virtual NIC provides access to the external network through a virtual switch that is   bridged through a Physical NIC to a physical network   (<a href="vim.host.NetworkConfig.md">HostNetworkConfig</a>.<a href="vim.host.NetworkConfig.md#vswitch">vswitch</a>[].<a href="vim.host.VirtualSwitch.Config.md#spec">spec</a>.<a href="vim.host.VirtualSwitch.Specification.md#bridge">bridge</a>)

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| device | string | None | None | Device name. |
| key | string | None | None | Linkable identifier. |
| portgroup | string | None | None | If the Virtual NIC is connecting to a vSwitch, this property is the name of   portgroup connected. If the Virtual NIC is connecting to a   DistributedVirtualSwitch, this property is an empty string. |
| spec | [vim.host.VirtualNic.Specification](vim.host.VirtualNic.Specification.md "vim.host.VirtualNic.Specification") | None | None | Configurable properties for the virtual network adapter object. |
| port | [vim.host.PortGroup.Port](vim.host.PortGroup.Port.md "vim.host.PortGroup.Port") | true | None | Port on the port group that the virtual network adapter is using    when it is enabled   (<a href="vim.dvs.DistributedVirtualPort.md">DistributedVirtualPort</a>.<a href="vim.dvs.DistributedVirtualPort.md#key">key</a>). |


