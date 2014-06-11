vim.host.VmfsDatastoreExpandSpec
================================
inherits from [vim.host.VmfsDatastoreSpec](docs/vim.host.VmfsDatastoreSpec.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Specification to increase the  capacity of a VMFS datastore by expanding   (increasing the size of) an existing extent of the datastore.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| partition | [vim.host.DiskPartitionInfo.Specification](vim.host.DiskPartitionInfo.Specification.md "vim.host.DiskPartitionInfo.Specification") | None | None | Partitioning specification. |
| extent | [vim.host.ScsiDisk.Partition](vim.host.ScsiDisk.Partition.md "vim.host.ScsiDisk.Partition") | None | None | VMFS extent to expand. |


