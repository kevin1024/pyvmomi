vim.vm.device.VirtualDiskOption.DeltaDiskFormatsSupported
=========================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


Delta disk format supported for each datastore type.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| datastoreType | string | None | None | Datastore type name |
| deltaDiskFormat | [vim.option.ChoiceOption](vim.option.ChoiceOption.md "vim.option.ChoiceOption") | None | None | Delta disk formats supported. Valid values are:   <ul>   <li><a href="vim.vm.device.VirtualDisk.DeltaDiskFormat.md#redoLogFormat">redoLogFormat</a>   <li><a href="vim.vm.device.VirtualDisk.DeltaDiskFormat.md#nativeFormat">nativeFormat</a>   </ul> |


