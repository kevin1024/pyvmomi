vim.host.DatastoreBrowser.FileInfo
==================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type contains rudimentary information about a file in a   datastore. The information here is not meant to cover all information in   traditional file systems, but rather to provide sufficient information for files   that are associated with virtual machines. Derived types describe the known file   types for a datastore.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| path | string | None | None | The path relative to the folder path in the search results. |
| fileSize | long | true | None | The size of the file in bytes. |
| modification | datetime | true | None | The last date and time the file was modified. |
| owner | string | true | None | The user name of the owner of the file. |


