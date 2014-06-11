vim.vm.device.VirtualEthernetCard.NetworkBackingInfo
====================================================
inherits from [vim.vm.device.VirtualDevice.DeviceBackingInfo](docs/vim.vm.device.VirtualDevice.DeviceBackingInfo.md)


The <a href="vim.vm.device.VirtualEthernetCard.NetworkBackingInfo.md">VirtualEthernetCardNetworkBackingInfo</a> data object   defines network backing for a virtual Ethernet card.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| network | [vim.Network](vim.Network.md "vim.Network") | true | None | Reference to the network managed object to which this backing applies.   This is not used during configuration. |
| inPassthroughMode | bool | true | None | &nbsp; |


