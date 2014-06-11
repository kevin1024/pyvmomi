vim.vm.device.VirtualControllerOption
=====================================
inherits from [vim.vm.device.VirtualDeviceOption](docs/vim.vm.device.VirtualDeviceOption.md)


The VirtualControllerOption data object type contains information about   a virtual controller type.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| devices | [vim.option.IntOption](vim.option.IntOption.md "vim.option.IntOption") | None | None | The minimum and maximum number of devices this controller can control   at run time. |
| supportedDevice | string | true | None | Array of supported device options for this controller. |


