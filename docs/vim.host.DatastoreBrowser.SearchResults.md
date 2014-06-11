vim.host.DatastoreBrowser.SearchResults
=======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type contains the results of a search method for one datastore. A   search method typically returns a set of these objects as an array.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| datastore | [vim.Datastore](vim.Datastore.md "vim.Datastore") | true | None | Datastore contains the results. |
| folderPath | string | true | None | Relative path to the top-level folder. |
| file | [vim.host.DatastoreBrowser.FileInfo](vim.host.DatastoreBrowser.FileInfo.md "vim.host.DatastoreBrowser.FileInfo") | true | None | Set of matching files, if any. |


