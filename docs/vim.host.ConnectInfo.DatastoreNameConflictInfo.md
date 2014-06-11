vim.host.ConnectInfo.DatastoreNameConflictInfo
==============================================
inherits from [vim.host.ConnectInfo.DatastoreInfo](docs/vim.host.ConnectInfo.DatastoreInfo.md)


This data object type describes a datastore on the host that has the same name as   a different datastore on VirtualCenter.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| newDatastoreName | string | None | None | To resolve a conflict with existing datastores, a suggested new name of the   datastore can be provided. |


