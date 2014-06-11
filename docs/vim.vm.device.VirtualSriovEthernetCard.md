vim.vm.device.VirtualSriovEthernetCard
======================================
inherits from [vim.vm.device.VirtualEthernetCard](docs/vim.vm.device.VirtualEthernetCard.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


The <a href="vim.vm.device.VirtualSriovEthernetCard.md">VirtualSriovEthernetCard</a> data object defines the properties   of a SR-IOV enabled Ethernet card attached to a virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| allowGuestOSMtuChange | bool | true | None | Indicates whether MTU can be changed from guest OS. |
| sriovBacking | [vim.vm.device.VirtualSriovEthernetCard.SriovBackingInfo](vim.vm.device.VirtualSriovEthernetCard.SriovBackingInfo.md "vim.vm.device.VirtualSriovEthernetCard.SriovBackingInfo") | true | None | Information about SR-IOV passthrough backing of this VirtualSriovEthernetCard. |


