vim.vm.device.VirtualDevice.DeviceBackingInfo
=============================================
inherits from [vim.vm.device.VirtualDevice.BackingInfo](docs/vim.vm.device.VirtualDevice.BackingInfo.md)


The <code><a href="vim.vm.device.VirtualDevice.DeviceBackingInfo.md">VirtualDeviceDeviceBackingInfo</a></code> data object type   defines information about a host device or resource that backs a device   in a virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| deviceName | string | None | None | The name of the device on the host system. |
| useAutoDetect | bool | true | None | Indicates whether the device should be auto detected  instead of directly specified. If this value is set to TRUE,  deviceName is ignored. |


