vim.StoragePod
==============
inherits from [vim.Folder](vim.Folder.md "vim.Folder")
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


The <a href="vim.StoragePod.md">StoragePod</a> data object aggregates the storage   resources of associated <a href="vim.Datastore.md">Datastore</a> objects into a single   storage resource for use by virtual machines. The storage services   such as Storage DRS (Distributed Resource Scheduling),   enhance the utility of the storage pod.   <p>   Use the <a href="vim.Folder.md">Folder</a>.<a href="vim.Folder.md#createStoragePod">CreateStoragePod</a> method   to create an instance of this object.   <p>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='summary'>summary</a> | [vim.StoragePod.Summary](vim.StoragePod.Summary.md "vim.StoragePod.Summary") | true | System.View | Storage pod summary. |
| <a href='podStorageDrsEntry'>podStorageDrsEntry</a> | [vim.StorageResourceManager.PodStorageDrsEntry](vim.StorageResourceManager.PodStorageDrsEntry.md "vim.StorageResourceManager.PodStorageDrsEntry") | true | System.Read | Storage DRS related attributes of the Storage Pod. |


