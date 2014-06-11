vim.host.DiskPartitionInfo.Specification
========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes the disk partition table    specification used to configure the partitions on a   disk.  This data object represents the fundamental data needed to specify   a partition table.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| partitionFormat | string | true | None | Partition format type on the disk. |
| chs | [vim.host.DiskDimensions.Chs](vim.host.DiskDimensions.Chs.md "vim.host.DiskDimensions.Chs") | true | None | Disk dimensions expressed as cylinder, head, sector (CHS)    coordinates. |
| totalSectors | long | true | None | Disk dimensions expressed in total number of    512-byte sectors. |
| partition | [vim.host.DiskPartitionInfo.Partition](vim.host.DiskPartitionInfo.Partition.md "vim.host.DiskPartitionInfo.Partition") | true | None | List of partitions on the disk. |


