vim.host.VffsVolume
===================
inherits from [vim.host.FileSystemVolume](docs/vim.host.FileSystemVolume.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


vFlash File System Volume.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| majorVersion | int | None | None | Major version number of VFFS. |
| version | string | None | None | Version string. Contains major and minor version numbers. |
| uuid | string | None | None | The universally unique identifier assigned to VFFS. |
| extent | [vim.host.ScsiDisk.Partition](vim.host.ScsiDisk.Partition.md "vim.host.ScsiDisk.Partition") | None | None | The list of partition names that comprise this disk's   VFFS extents. |


