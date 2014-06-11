vim.VirtualMachine.WipeResult
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


Data structure used by wipeDisk to return the amount of disk space that  can be saved on an Flex-SE disk if a subsequent shrinkDisk API is invoked  on that disk.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| diskId | int | None | None | The disk id for the disk that was wiped. |
| shrinkableDiskSpace | long | None | None | The amount of shrinkable disk space in kB. |


