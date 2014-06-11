vim.host.VmfsDatastoreOption.SingleExtentInfo
=============================================
inherits from [vim.host.VmfsDatastoreOption.Info](docs/vim.host.VmfsDatastoreOption.Info.md)


Datastore addition policy to use a single extent on the disk for a VMFS   datastore.  A single extent implies that one disk partition will be   created on the disk for creating or increasing the capacity of a VMFS datastore.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vmfsExtent | [vim.host.DiskPartitionInfo.BlockRange](vim.host.DiskPartitionInfo.BlockRange.md "vim.host.DiskPartitionInfo.BlockRange") | None | None | The block range to be used as an extent in a VMFS datastore. |


