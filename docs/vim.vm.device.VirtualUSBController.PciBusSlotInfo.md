vim.vm.device.VirtualUSBController.PciBusSlotInfo
=================================================
inherits from [vim.vm.device.VirtualDevice.PciBusSlotInfo](docs/vim.vm.device.VirtualDevice.PciBusSlotInfo.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


The <code>PciBusSlotInfo</code> data object type   defines information about the pci bus slots of usb controller device   in a virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ehciPciSlotNumber | int | true | None | The pci slot number of eHCI controller.   <p>   This property should be used only when the ehciEnabled property   is set to true. |


