vim.host.DiskPartitionInfo
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Information about the partitions on a disk.  A DiskPartitionInfo object   provides two different views into the partitions on a disk:      <p>   <ul>   <li>A detailed specification that is used to create the partition   table.   <li>A convenient view that shows the allocations   of blocks as a contiguous sequence of block ranges.   </ul><br>See <a href="vim.host.StorageSystem.md#retrieveDiskPartitionInfo">RetrieveDiskPartitionInfo</a><br>See <a href="vim.host.StorageSystem.md#computeDiskPartitionInfo">ComputeDiskPartitionInfo</a><br>See <a href="vim.host.StorageSystem.md#updateDiskPartitions">UpdateDiskPartitions</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| deviceName | string | None | None | The device name of the disk to which this partition information   corresponds. |
| spec | [vim.host.DiskPartitionInfo.Specification](vim.host.DiskPartitionInfo.Specification.md "vim.host.DiskPartitionInfo.Specification") | None | None | The detailed disk partition specification.  Use this specification for   manipulating the file system.<br>See <a href="vim.host.StorageSystem.md#retrieveDiskPartitionInfo">RetrieveDiskPartitionInfo</a><br>See <a href="vim.host.StorageSystem.md#updateDiskPartitions">UpdateDiskPartitions</a><br> |
| layout | [vim.host.DiskPartitionInfo.Layout](vim.host.DiskPartitionInfo.Layout.md "vim.host.DiskPartitionInfo.Layout") | None | None | A convenient format for describing disk layout.  This layout    specification can be converted to a Specification object.<br>See <a href="vim.host.StorageSystem.md#computeDiskPartitionInfo">ComputeDiskPartitionInfo</a><br> |


