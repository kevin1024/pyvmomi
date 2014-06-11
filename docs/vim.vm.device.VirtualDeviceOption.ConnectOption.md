vim.vm.device.VirtualDeviceOption.ConnectOption
===============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The ConnectOption data object type contains information about options for   connectable virtual devices.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| startConnected | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | None | None | Flag to indicate whether or not the device supports   the startConnected feature. |
| allowGuestControl | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | None | None | Flag to indicate whether or not the device can be   connected and disconnected from within the guest operating system. |


