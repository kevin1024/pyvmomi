vim.vm.device.VirtualPCIPassthrough.DeviceBackingInfo
=====================================================
inherits from [vim.vm.device.VirtualDevice.DeviceBackingInfo](docs/vim.vm.device.VirtualDevice.DeviceBackingInfo.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The VirtualPCIPassthrough.DeviceBackingInfo data object type    contains information about the backing that maps the    virtual device onto a physical device.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | string | None | None | The name ID of this PCI, composed of "bus:slot.function". |
| deviceId | string | None | None | The device ID of this PCI. You must use the device ID retrieved  from the vSphere host (<a href="vim.host.PciDevice.md">HostPciDevice</a>.deviceId), converted  as is to a string. |
| systemId | string | None | None | The ID of the system the PCI device is attached to. |
| vendorId | short | None | None | The vendor ID for this PCI device. You must use the vendor ID retrieved  from the vSphere host (<a href="vim.host.PciDevice.md">HostPciDevice</a>.vendorId). |


