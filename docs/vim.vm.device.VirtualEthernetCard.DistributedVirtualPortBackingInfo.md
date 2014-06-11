vim.vm.device.VirtualEthernetCard.DistributedVirtualPortBackingInfo
===================================================================
inherits from [vim.vm.device.VirtualDevice.BackingInfo](docs/vim.vm.device.VirtualDevice.BackingInfo.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.vm.device.VirtualEthernetCard.DistributedVirtualPortBackingInfo.md">VirtualEthernetCardDistributedVirtualPortBackingInfo</a>  data object defines backing for a virtual Ethernet card that connects  to a distributed virtual switch port or portgroup.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| port | [vim.dvs.PortConnection](vim.dvs.PortConnection.md "vim.dvs.PortConnection") | None | None | <a href="vim.dvs.DistributedVirtualPort.md">DistributedVirtualPort</a> or <a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a>   connection. To specify a port connection, set the   <a href="vim.dvs.PortConnection.md#portKey">portKey</a> property.   To specify a portgroup connection, set the   <a href="vim.dvs.PortConnection.md#portgroupKey">portgroupKey</a> property.   <p>   This property will be unset during Virtual Machine or template cloning   operation unless it's set to a <a href="vim.dvs.PortConnection.md">DistributedVirtualSwitchPortConnection</a>    object and the portgroup is a late binding portgroup. |


