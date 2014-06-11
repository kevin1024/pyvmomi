vim.vm.device.VirtualPointingDeviceOption.DeviceBackingOption
=============================================================
inherits from [vim.vm.device.VirtualDeviceOption.DeviceBackingOption](docs/vim.vm.device.VirtualDeviceOption.DeviceBackingOption.md)


The DeviceBackingOption data object type represents   the options for a pointing device backing a   VirtualPointingDevice data object type.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| hostPointingDevice | [vim.option.ChoiceOption](vim.option.ChoiceOption.md "vim.option.ChoiceOption") | None | None | This object defines the supported mouse types, including the default    supported mouse type, with the following properties:   <p>   <ul>   <li><b>hostPointingDevices.value</b>:  This array defines the    supported mouse types.   <li><b>hostPointingDevices.choiceDescription</b>: This array    provides the descriptions for the supported mouse types defined by    hostPointingDevices.value.   <li><b>hostPointingDevices.defaultIndex</b>: This integer points    to an index in the hostPointingDevices.value array.  This is the    mouse type supported by default.   </ul> |


