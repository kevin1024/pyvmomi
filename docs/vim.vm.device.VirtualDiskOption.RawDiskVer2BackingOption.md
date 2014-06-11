vim.vm.device.VirtualDiskOption.RawDiskVer2BackingOption
========================================================
inherits from [vim.vm.device.VirtualDeviceOption.DeviceBackingOption](docs/vim.vm.device.VirtualDeviceOption.DeviceBackingOption.md)


The VirtualDiskOption.RawDiskVer2BackingOption object type   contains the available options when backing a virtual disk   using a host device on VMware Server.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| descriptorFileNameExtensions | [vim.option.ChoiceOption](vim.option.ChoiceOption.md "vim.option.ChoiceOption") | None | None | Valid extensions for the filename of the raw disk descriptor   file. |
| uuid | bool | None | None | Flag to indicate whether this backing supports disk UUID property. |


