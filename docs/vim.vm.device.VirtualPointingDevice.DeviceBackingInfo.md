vim.vm.device.VirtualPointingDevice.DeviceBackingInfo
=====================================================
inherits from [vim.vm.device.VirtualDevice.DeviceBackingInfo](docs/vim.vm.device.VirtualDevice.DeviceBackingInfo.md)


The VirtualPointingDevice.DeviceBackingInfo provides information about    the physical mouse backing the VirtualPointingDevice data object    type.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| hostPointingDevice | string | None | None | This optional property defines the mouse type (two-button,    three-button, and so on).  The mouse type    determines how the user interacts with the host mouse.     The valid values are specified in the     <a href="vim.vm.device.VirtualPointingDeviceOption.DeviceBackingOption.HostPointingDeviceChoice.md">VirtualPointingDeviceHostChoice</a> list.   <p>   <b>Note</b>:  The value specified by this property must be    one of the supported types listed in the hostPointingDevices.value    array in the <a href="vim.vm.device.VirtualPointingDeviceOption.md">VirtualPointingDeviceOption</a> data object type.  If this property is    not set, then the property defaults to the    hostPointingDevices.defaultIndex property in the same data    object type. |


