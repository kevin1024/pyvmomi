vim.host.VmfsDatastoreOption.MultipleExtentInfo
===============================================
inherits from [vim.host.VmfsDatastoreOption.Info](docs/vim.host.VmfsDatastoreOption.Info.md)


Datastore addition policy to use multiple extents on the disk for a VMFS   datastore.  Multiple extents implies that more than one disk partition   will be created on the disk for creating or increasing the capacity of a   VMFS datastore.   Multiple extents are needed when unpartitioned space is fragmented in the   existing partition layout of the disk.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vmfsExtent | [vim.host.DiskPartitionInfo.BlockRange](vim.host.DiskPartitionInfo.BlockRange.md "vim.host.DiskPartitionInfo.BlockRange") | None | None | The block ranges to be used as extents in a VMFS datastore.  The first   block range will be the head partition. |


