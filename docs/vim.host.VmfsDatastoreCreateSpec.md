vim.host.VmfsDatastoreCreateSpec
================================
inherits from [vim.host.VmfsDatastoreSpec](docs/vim.host.VmfsDatastoreSpec.md)


This data object type is used when creating a new VMFS datastore,   to create a specification for the VMFS datastore.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| partition | [vim.host.DiskPartitionInfo.Specification](vim.host.DiskPartitionInfo.Specification.md "vim.host.DiskPartitionInfo.Specification") | None | None | Partitioning specification. |
| vmfs | [vim.host.VmfsVolume.Specification](vim.host.VmfsVolume.Specification.md "vim.host.VmfsVolume.Specification") | None | None | The VMFS creation specification. |
| extent | [vim.host.ScsiDisk.Partition](vim.host.ScsiDisk.Partition.md "vim.host.ScsiDisk.Partition") | true | None | Extents to append to VMFS. |


