vim.VirtualDiskManager.VirtualDiskSpec
======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


Specification used to create or clone a virtual disk

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| diskType | string | None | None | The type of the new virtual disk.<br>See <a href="vim.VirtualDiskManager.VirtualDiskType.md">VirtualDiskType</a><br> |
| adapterType | string | None | None | The type of the virtual disk adapter for the new virtual disk.<br>See <a href="vim.VirtualDiskManager.VirtualDiskAdapterType.md">VirtualDiskAdapterType</a><br> |


