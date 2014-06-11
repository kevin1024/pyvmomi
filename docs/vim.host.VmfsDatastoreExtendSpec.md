vim.host.VmfsDatastoreExtendSpec
================================
inherits from [vim.host.VmfsDatastoreSpec](docs/vim.host.VmfsDatastoreSpec.md)


Specification to increase the capacity of a VMFS datastore by adding   one or more new extents to the datastore.  All the extents to be added   must be on the same disk.  Extension is different   from creation in that the VMFS creation specification need not be   specified.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| partition | [vim.host.DiskPartitionInfo.Specification](vim.host.DiskPartitionInfo.Specification.md "vim.host.DiskPartitionInfo.Specification") | None | None | Partitioning specification. |
| extent | [vim.host.ScsiDisk.Partition](vim.host.ScsiDisk.Partition.md "vim.host.ScsiDisk.Partition") | None | None | Extents to append to VMFS. |


