vim.DatastoreNamespaceManager
=============================
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


The DatastoreNamespaceManager managed object exposes APIs for  manipulating top-level directories of datastores which do not  support the traditional top-level directory creation.<br>See <a href="vim.Datastore.Capability.md#topLevelDirectoryCreateSupported">topLevelDirectoryCreateSupported</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


CreateDirectory([datastore](vim.Datastore.md "vim.Datastore"), [displayName](#string "string"), [policy](#string "string"))
---------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.FileAlreadyExists](vim.fault.FileAlreadyExists.md "vim.fault.FileAlreadyExists"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.CannotCreateFile](vim.fault.CannotCreateFile.md "vim.fault.CannotCreateFile")

---
| service name | CreateDirectory |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version9) |
| privilege    | Datastore.Config |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.CannotCreateFile](vim.fault.CannotCreateFile.md "vim.fault.CannotCreateFile") | if a general system error occurred while creating                      directory on the datastore<br>See <a href="vim.DatastoreNamespaceManager.md#DeleteDirectory">DeleteDirectory</a><br> |
| [vim.fault.FileAlreadyExists](vim.fault.FileAlreadyExists.md "vim.fault.FileAlreadyExists") | if the given directory already exists<br>See <a href="vim.DatastoreNamespaceManager.md#DeleteDirectory">DeleteDirectory</a><br> |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the given datastore is not supported by                           the DatastoreNamespaceManage<br>See <a href="vim.DatastoreNamespaceManager.md#DeleteDirectory">DeleteDirectory</a><br> |




DeleteDirectory([datacenter](vim.Datacenter.md "vim.Datacenter"), [datastorePath](#string "string"))
----------------------------------------------------------------------------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.InvalidDatastorePath](vim.fault.InvalidDatastorePath.md "vim.fault.InvalidDatastorePath"), [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound")

---
| service name | DeleteDirectory |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version9) |
| privilege    | Datastore.Config |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if a generic system error happened.<br>See <a href="vim.DatastoreNamespaceManager.md#CreateDirectory">CreateDirectory</a><br> |
| [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound") | if the given directory can not be found<br>See <a href="vim.DatastoreNamespaceManager.md#CreateDirectory">CreateDirectory</a><br> |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the given datastore is not supported by                           the DatastoreNamespaceManager<br>See <a href="vim.DatastoreNamespaceManager.md#CreateDirectory">CreateDirectory</a><br> |
| [vim.fault.InvalidDatastorePath](vim.fault.InvalidDatastorePath.md "vim.fault.InvalidDatastorePath") | if the given path is not a top-level directory<br>See <a href="vim.DatastoreNamespaceManager.md#CreateDirectory">CreateDirectory</a><br> |




