vim.host.NasDatastoreInfo
=========================
inherits from [vim.Datastore.Info](docs/vim.Datastore.Info.md)


Information details about a network-attached storage   (NAS) datastore.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| nas | [vim.host.NasVolume](vim.host.NasVolume.md "vim.host.NasVolume") | true | None | The NFS mount information for the datastore.  May not   be available when the datastore is not accessible. |


