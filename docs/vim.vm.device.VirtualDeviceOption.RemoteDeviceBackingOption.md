vim.vm.device.VirtualDeviceOption.RemoteDeviceBackingOption
===========================================================
inherits from [vim.vm.device.VirtualDeviceOption.BackingOption](docs/vim.vm.device.VirtualDeviceOption.BackingOption.md)


VirtualDeviceOption.RemoteDeviceBackingOption describes the options   for a remote device backing. The primary difference   between a remote device backing and a local device backing is that   the VirtualCenter server cannot provide a list of remote host devices   available for this virtual device backing.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| autoDetectAvailable | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | None | None | Flag to indicate whether the specific instance of this device can  be auto-detected on the host instead of having to specify a  particular physical device. |


