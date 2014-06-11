vim.vm.device.VirtualSriovEthernetCard.SriovBackingInfo
=======================================================
inherits from [vim.vm.device.VirtualDevice.BackingInfo](docs/vim.vm.device.VirtualDevice.BackingInfo.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


The <a href="vim.vm.device.VirtualSriovEthernetCard.SriovBackingInfo.md">VirtualSriovEthernetCardSriovBackingInfo</a>   data object contains information about the SR-IOV physical function and   virtual function backing for a passthrough NIC.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| physicalFunctionBacking | [vim.vm.device.VirtualPCIPassthrough.DeviceBackingInfo](vim.vm.device.VirtualPCIPassthrough.DeviceBackingInfo.md "vim.vm.device.VirtualPCIPassthrough.DeviceBackingInfo") | true | None |  |
| virtualFunctionBacking | [vim.vm.device.VirtualPCIPassthrough.DeviceBackingInfo](vim.vm.device.VirtualPCIPassthrough.DeviceBackingInfo.md "vim.vm.device.VirtualPCIPassthrough.DeviceBackingInfo") | true | None |  |
| virtualFunctionIndex | int | true | None |  |


