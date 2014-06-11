vim.host.ScsiDisk
=================
inherits from [vim.host.ScsiLun](docs/vim.host.ScsiLun.md)


This data object type describes a SCSI disk.  A SCSI disk contains a    partition table which can be changed.   To change a SCSI disk, use the device name and the partition specification.<br>See <a href="vim.host.StorageSystem.md#retrieveDiskPartitionInfo">RetrieveDiskPartitionInfo</a><br>See <a href="vim.host.StorageSystem.md#updateDiskPartitions">UpdateDiskPartitions</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| capacity | [vim.host.DiskDimensions.Lba](vim.host.DiskDimensions.Lba.md "vim.host.DiskDimensions.Lba") | None | None | The size of SCSI disk using the Logical Block Addressing scheme. |
| devicePath | string | None | None | The device path of the ScsiDisk.  This device path is a file path   that can be opened to create partitions on the disk.<br>See <a href="vim.host.StorageSystem.md#retrieveDiskPartitionInfo">RetrieveDiskPartitionInfo</a><br>See <a href="vim.host.StorageSystem.md#updateDiskPartitions">UpdateDiskPartitions</a><br> |
| ssd | bool | true | None | Indicates whether the ScsiDisk is SSD backed.  If unset, the information whether the ScsiDisk is SSD backed  is unknown. |


