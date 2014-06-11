vim.host.DiskPartitionInfo.Partition
====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Information about a single disk partition.  A partition is a contiguous   set of blocks on a disk that is marked for use.  The typeId identifies   the purpose of the data in the partition.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| partition | int | None | None | The partition number.  Must be a positive integer. |
| startSector | long | None | None | The start sector. |
| endSector | long | None | None | The end sector. |
| type | string | None | None | Type of data in the partition.  If it is a well-known partition type,   it will be one of the defined types.  If it is not, then it will be   reported as a hexadecimal number.  For example, "none", "vmfs", "linux",   and "0x20" are all valid values.<br>See <a href="vim.host.DiskPartitionInfo.Type.md">HostDiskPartitionInfoType</a><br> |
| guid | string | true | None | Globally Unique Identifier of the partition, as defined by the GUID  Partition Table (GPT) format. This is available only for GPT formatted  disks. |
| logical | bool | None | None | The flag to indicate whether or not the partition is    logical.  If true, the partition    number should be greater than 4. |
| attributes | int | None | None | The attributes on the partition. |
| partitionAlignment | long | true | None | Partition alignment in bytes.  If unset, partition alignment value is unknown. |


