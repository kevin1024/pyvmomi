vim.host.ConnectInfo.DatastoreExistsInfo
========================================
inherits from [vim.host.ConnectInfo.DatastoreInfo](docs/vim.host.ConnectInfo.DatastoreInfo.md)


This data object type describes a datastore on the host that matches an existing   datastore on VirtualCenter that has a different name.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| newDatastoreName | string | None | None | The name of a matching datastore on VirtualCenter. The datastore on the host   will be renamed to this name. |


