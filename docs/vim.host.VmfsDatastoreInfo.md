vim.host.VmfsDatastoreInfo
==========================
inherits from [vim.Datastore.Info](docs/vim.Datastore.Info.md)


Information details about a VMFS datastore.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| maxPhysicalRDMFileSize | long | None | None | Maximum raw device mapping size (physical compatibility) |
| maxVirtualRDMFileSize | long | None | None | Maximum raw device mapping size (virtual compatibility) |
| vmfs | [vim.host.VmfsVolume](vim.host.VmfsVolume.md "vim.host.VmfsVolume") | true | None | The VMFS volume information for the datastore.  May not be   available when the datastore is not accessible. |


