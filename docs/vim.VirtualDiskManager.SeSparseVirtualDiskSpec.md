vim.VirtualDiskManager.SeSparseVirtualDiskSpec
==============================================
inherits from [vim.VirtualDiskManager.FileBackedVirtualDiskSpec](docs/vim.VirtualDiskManager.FileBackedVirtualDiskSpec.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


Specification used to create an Flex-SE based virtual disk

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| grainSizeKb | int | true | None | The grain size in kB for Flex-SE disk types. Default value will  be used if unset. |


