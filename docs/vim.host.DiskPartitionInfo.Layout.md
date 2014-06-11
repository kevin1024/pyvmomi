vim.host.DiskPartitionInfo.Layout
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes the disk partition layout    specified as a list of ordered BlockRanges.  This   view of the disk partitions shows the data on the disk as a contiguous   set of BlockRanges.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| total | [vim.host.DiskDimensions.Lba](vim.host.DiskDimensions.Lba.md "vim.host.DiskDimensions.Lba") | true | None | Total number of blocks on a disk. |
| partition | [vim.host.DiskPartitionInfo.BlockRange](vim.host.DiskPartitionInfo.BlockRange.md "vim.host.DiskPartitionInfo.BlockRange") | None | None | List of block ranges on the disk. |


