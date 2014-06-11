vim.vm.device.VirtualDevice.RemoteDeviceBackingInfo
===================================================
inherits from [vim.vm.device.VirtualDevice.BackingInfo](docs/vim.vm.device.VirtualDevice.BackingInfo.md)


<code><a href="vim.vm.device.VirtualDevice.RemoteDeviceBackingInfo.md">VirtualDeviceRemoteDeviceBackingInfo</a></code> is a data object type   for information   about a remote device backing used by a device in a virtual machine.   The primary difference between a remote device backing and a   local device backing is that the VirtualCenter server cannot provide a list   of remote host devices available for this virtual device backing.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| deviceName | string | None | None | The name of the device on the remote system. |
| useAutoDetect | bool | true | None | Indicates whether the device should be auto detected  instead of directly specified. If this value is set to TRUE,  <code>deviceName</code> is ignored. |


