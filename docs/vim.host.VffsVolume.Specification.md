vim.host.VffsVolume.Specification
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This data object type describes the VFFS   creation specification.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| devicePath | string | None | None | The device path of the SSD disk.<br>See <a href="vim.host.ScsiDisk.md#devicePath">devicePath</a><br> |
| partition | [vim.host.DiskPartitionInfo.Specification](vim.host.DiskPartitionInfo.Specification.md "vim.host.DiskPartitionInfo.Specification") | true | None | Partition specification of the SSD disk. If this property  is not provided, partition information will be computed  and generated. |
| majorVersion | int | None | None | Major version number of VFFS.  This can be changed if the VFFS is   upgraded, but this is an irreversible change. |
| volumeName | string | None | None | Volume name of VFFS. |


