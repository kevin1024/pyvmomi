vim.FileManager
===============
as of [VI API 2.5](vim.version.md#vim.version.version2)


This managed object type provides a way to manage and manipulate files and   folders on datastores. The source and the destination names are in the form of   a URL or a datastore path.   <p>   A URL has the form   <blockquote><i>scheme</i>://<i>authority</i>/folder/<i>path</i>?dcPath=<i>dcPath</i>&dsName=<i>dsName</i></blockquote>   where   <li><i>scheme</i> is <code>http</code> or <code>https</code>.</li>   <li><i>authority</i> specifies the hostname or IP address of the VirtualCenter or   ESX server and optionally the port.</li>   <li><i>dcPath</i> is the inventory path to the Datacenter containing the    Datastore.</li>   <li><i>dsName</i> is the name of the Datastore.</li>   <li><i>path</i> is a slash-delimited path from the root of the datastore.</li>   <p>   A datastore path has the form <blockquote>[<i>datastore</i>] <i>path</i></blockquote>   where   <li><i>datastore</i> is the datastore name.</li>   <li><i>path</i> is a slash-delimited path from the root of the datastore.</li>   An example datastore path is "[storage] path/to/file.extension".   A listing of all the files, disks and folders on   a datastore can be obtained from the datastore browser.<br>See <a href="vim.host.DatastoreBrowser.md">HostDatastoreBrowser</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


MoveDatastoreFile([sourceName](#string "string"), [sourceDatacenter](vim.Datacenter.md "vim.Datacenter"), [destinationName](#string "string"), [destinationDatacenter](vim.Datacenter.md "vim.Datacenter"))
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.FileLocked](vim.fault.FileLocked.md "vim.fault.FileLocked"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.CannotAccessFile](vim.fault.CannotAccessFile.md "vim.fault.CannotAccessFile"), [vim.fault.FileAlreadyExists](vim.fault.FileAlreadyExists.md "vim.fault.FileAlreadyExists"), [vim.fault.NoDiskSpace](vim.fault.NoDiskSpace.md "vim.fault.NoDiskSpace"), [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound")

---
| service name | MoveDatastoreFile |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | dynamic |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the source   or destination datastores. Typically, a specific subclass of this exception is   thrown. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a generic file error |
| [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound") | if the file or folder specified by sourceName is not   found, or, any intermediate level folder specified by the destinationName is not   found. |
| [vim.fault.CannotAccessFile](vim.fault.CannotAccessFile.md "vim.fault.CannotAccessFile") | if the source file or folder cannot be moved because of   insufficient permissions. |
| [vim.fault.FileLocked](vim.fault.FileLocked.md "vim.fault.FileLocked") | if the source file or folder is currently locked or in use. |
| [vim.fault.FileAlreadyExists](vim.fault.FileAlreadyExists.md "vim.fault.FileAlreadyExists") | if a file with the given name already   exists at the destination, and the force flag is false. For folders, if the   destination exists, this fault is thrown regardless. |
| [vim.fault.NoDiskSpace](vim.fault.NoDiskSpace.md "vim.fault.NoDiskSpace") | if there is not enough space available on the destination   datastore. |




CopyDatastoreFile([sourceName](#string "string"), [sourceDatacenter](vim.Datacenter.md "vim.Datacenter"), [destinationName](#string "string"), [destinationDatacenter](vim.Datacenter.md "vim.Datacenter"))
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.FileLocked](vim.fault.FileLocked.md "vim.fault.FileLocked"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.CannotAccessFile](vim.fault.CannotAccessFile.md "vim.fault.CannotAccessFile"), [vim.fault.FileAlreadyExists](vim.fault.FileAlreadyExists.md "vim.fault.FileAlreadyExists"), [vim.fault.NoDiskSpace](vim.fault.NoDiskSpace.md "vim.fault.NoDiskSpace"), [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound")

---
| service name | CopyDatastoreFile |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | dynamic |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the source   or destination datastores. Typically, a specific subclass of this exception is   thrown. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a generic file error |
| [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound") | if the file or folder specified by sourceName is not   found, or, any intermediate level folder specified by the destinationName is not   found. |
| [vim.fault.CannotAccessFile](vim.fault.CannotAccessFile.md "vim.fault.CannotAccessFile") | if the source cannot be accessed because of   insufficient permissions. |
| [vim.fault.FileLocked](vim.fault.FileLocked.md "vim.fault.FileLocked") | if the source file or folder is currently locked or in use. |
| [vim.fault.FileAlreadyExists](vim.fault.FileAlreadyExists.md "vim.fault.FileAlreadyExists") | if a file with the given name already   exists at the destination, and the force flag is false. |
| [vim.fault.NoDiskSpace](vim.fault.NoDiskSpace.md "vim.fault.NoDiskSpace") | if there is not enough space available at the destination   datastore. |




DeleteDatastoreFile([name](#string "string"), [datacenter](vim.Datacenter.md "vim.Datacenter"))
-----------------------------------------------------------------------------------------------
 raises [vim.fault.CannotDeleteFile](vim.fault.CannotDeleteFile.md "vim.fault.CannotDeleteFile"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound"), [vim.fault.FileLocked](vim.fault.FileLocked.md "vim.fault.FileLocked")

---
| service name | DeleteDatastoreFile |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | dynamic |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the   datastore. Typically, a specific subclass of this exception is thrown. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a generic file error |
| [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound") | if the file or folder specified by name   is not found. |
| [vim.fault.CannotDeleteFile](vim.fault.CannotDeleteFile.md "vim.fault.CannotDeleteFile") | if the delete operation on the file or folder   fails. |
| [vim.fault.FileLocked](vim.fault.FileLocked.md "vim.fault.FileLocked") | if the source file or folder  is currently locked or   in use. |




MakeDirectory([name](#string "string"), [datacenter](vim.Datacenter.md "vim.Datacenter"))
-----------------------------------------------------------------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound"), [vim.fault.CannotCreateFile](vim.fault.CannotCreateFile.md "vim.fault.CannotCreateFile"), [vim.fault.FileAlreadyExists](vim.fault.FileAlreadyExists.md "vim.fault.FileAlreadyExists")

---
| service name | MakeDirectory |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | dynamic |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the   datastore. Typically, a specific subclass of this exception is thrown. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a generic file error |
| [vim.fault.CannotCreateFile](vim.fault.CannotCreateFile.md "vim.fault.CannotCreateFile") | if the create operation on the folder fails. |
| [vim.fault.FileAlreadyExists](vim.fault.FileAlreadyExists.md "vim.fault.FileAlreadyExists") | if a file or folder with the given name already   exists at the destination. |
| [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound") | if the createParentDirectories is false and a intermediate   level folder specified by name is not found. |




ChangeOwner([name](#string "string"), [datacenter](vim.Datacenter.md "vim.Datacenter"), [owner](#string "string"))
------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.UserNotFound](vim.fault.UserNotFound.md "vim.fault.UserNotFound")

---
| service name | ChangeOwner |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#vim.version.version2) |
| privilege    | dynamic |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | vim.fault.InvalidDatastore |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | vim.fault.FileFault |
| [vim.fault.UserNotFound](vim.fault.UserNotFound.md "vim.fault.UserNotFound") | vim.fault.UserNotFound |




