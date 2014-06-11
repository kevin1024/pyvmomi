vim.host.DiskPartitionInfo.BlockRange
=====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


A BlockRange data object type describes a contiguous set of blocks    on a disk.  A BlockRange may describe either a partition or    unpartitioned (primordial) blocks on the disk.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| partition | int | true | None | Partition number.  This number is a hint from the server indicating   what the partition number for this block range is if the range   corresponds to a partition.  The partition number should correlate to   the one in the partition specification.  If sent back to the server,   this property is ignored. |
| type | string | None | None | The type of data in the partition.<br>See <a href="vim.host.DiskPartitionInfo.Partition.md#type">type</a><br> |
| start | [vim.host.DiskDimensions.Lba](vim.host.DiskDimensions.Lba.md "vim.host.DiskDimensions.Lba") | None | None | The starting block address of the disk range.  The block numbers start   from zero.  The range is inclusive of the end address. |
| end | [vim.host.DiskDimensions.Lba](vim.host.DiskDimensions.Lba.md "vim.host.DiskDimensions.Lba") | None | None | The end block address of the disk range.  The block numbers start   from zero.  The range is inclusive of the end address. |


