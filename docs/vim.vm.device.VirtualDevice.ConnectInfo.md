vim.vm.device.VirtualDevice.ConnectInfo
=======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The <code><a href="vim.vm.device.VirtualDevice.ConnectInfo.md">VirtualDeviceConnectInfo</a></code> data object type   contains information about connectable virtual devices.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| startConnected | bool | None | None | Specifies whether or not to connect the device   when the virtual machine starts. |
| allowGuestControl | bool | None | None | Enables guest control over whether the connectable device is   connected. |
| connected | bool | None | None | Indicates whether the device is currently connected.   Valid only while the virtual machine is running. |
| status | string | true | None | Indicates the current status of the connectable device. Valid only while the   virtual machine is running. The set of possible values is described in   <a href="vim.vm.device.VirtualDevice.ConnectInfo.Status.md">VirtualDeviceConnectInfoStatus</a> |


