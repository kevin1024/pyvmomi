vim.vm.device.VirtualDiskOption.RawDiskMappingVer1BackingOption
===============================================================
inherits from [vim.vm.device.VirtualDeviceOption.DeviceBackingOption](docs/vim.vm.device.VirtualDeviceOption.DeviceBackingOption.md)


The VirtualDiskOption.RawDiskMappingVer1BackingOption object type   contains the available options when backing a virtual disk using   a raw device mapping on ESX Server 2.5 or 3.x.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| descriptorFileNameExtensions | [vim.option.ChoiceOption](vim.option.ChoiceOption.md "vim.option.ChoiceOption") | true | None | Valid extensions for the filename of the optional   raw disk mapping descriptor file.   This is present only for ESX Server 3.x and greater hosts. |
| compatibilityMode | [vim.option.ChoiceOption](vim.option.ChoiceOption.md "vim.option.ChoiceOption") | None | None | The supported raw disk mapping compatibility modes.<br>See <a href="vim.vm.device.VirtualDiskOption.CompatibilityMode.md">VirtualDiskCompatibilityMode</a><br> |
| diskMode | [vim.option.ChoiceOption](vim.option.ChoiceOption.md "vim.option.ChoiceOption") | None | None | The disk mode. Valid values are:   <ul>   <li><a href="vim.vm.device.VirtualDiskOption.DiskMode.md#persistent">persistent</a>   <li><a href="vim.vm.device.VirtualDiskOption.DiskMode.md#independent_persistent">independent_persistent</a>   <li><a href="vim.vm.device.VirtualDiskOption.DiskMode.md#independent_nonpersistent">independent_nonpersistent</a>   </ul><br>See <a href="vim.vm.device.VirtualDiskOption.DiskMode.md">VirtualDiskMode</a><br> |
| uuid | bool | None | None | Flag to indicate whether this backing supports disk UUID property. |


