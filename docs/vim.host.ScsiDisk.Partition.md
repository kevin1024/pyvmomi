vim.host.ScsiDisk.Partition
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes the specification of a Disk partition.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| diskName | string | None | None | The SCSI disk device on which a VMware File System (VMFS)    extent resides.<br>See <a href="vim.host.ScsiDisk.md">HostScsiDisk</a><br>See <a href="vim.host.ScsiLun.md#canonicalName">canonicalName</a><br> |
| partition | int | None | None | The partition number of the partition on the ScsiDisk. |


