vim.host.DatastoreBrowser
=========================


The DatastoreBrowser managed object type provides access to the contents of one or   more datastores. The items in a datastore are files that contain configuration,   virtual disk, and the other data associated with a virtual machine.   <p>   Although datastores may often be implemented using a traditional file system, a full   interface to a file system is not provided here. Instead, specialized access for   virtual machine files is provided. A datastore implementation may completely hide the   file directory structure.   <p>   The intent is to provide functionality analogous to a file chooser in a user   interface.   <p>   Files on datastores do not have independent permissions through this API. Instead,   the permissions for all the files on a datastore derive from the datastore object   itself. It is not possible to change individual file permissions as the user browsing   the datastore may not necessarily be a recognized user from the point of view of the   host changing the permission. This occurs if the user browsing the datastore is doing   so through the VirtualCenter management server.   <p>   The DatastoreBrowser provides many ways to customize a search for files. A search can   be customized by specifying the types of files to be searched, search criteria   specific to a file type, and the amount of detail about each file. The most basic   queries only use file details and are efficient with limited side effects. For these   queries, file metadata details can be optionally retrieved, but the files themselves   are opened and their contents examined. As a result, these files are not necessarily   validated.   <p>   More complicated queries can be formed by specifying the specific types of files to   be searched, the parameters to filter for each type, and the desired level of detail   about each file. This method of searching for files is convenient because it allows   additional data about the virtual machine component to be retrieved. In addition,   certain validation checks can be performed on matched files as an inherent part of   the details collection process. However, gathering extra details or the use of type   specific filters can sometimes only be implemented by examining the contents of a   file. As a result, the use of these conveniences comes with the cost of additional   latency in the request and possible side effects on the system as a whole.   <p>   The DatastoreBrowser is referenced from various objects, including from   <a href="vim.Datastore.md">Datastore</a>, <a href="vim.ComputeResource.md">ComputeResource</a>, <a href="vim.HostSystem.md">HostSystem</a> and   <a href="vim.VirtualMachine.md">VirtualMachine</a>.  Depending on which object is used, there are different   requirements for the accessibility of the browsed datastore from the host (or hosts)   associated with the object:   <ul>      <li> When referenced from the target <a href="vim.Datastore.md">Datastore</a>, it needs to be           accessible from at least one host on which the datastore is mounted.           See <a href="vim.Datastore.Summary.md#accessible">accessible</a>.      <li> When referenced from a <a href="vim.ComputeResource.md">ComputeResource</a>, the target datastore           needs to be accessible from at least one host in the ComputeResource.           See <a href="vim.host.MountInfo.md#accessible">accessible</a>.      <li> When referenced from a <a href="vim.HostSystem.md">HostSystem</a>, the target datastore needs           to be accessible from that host. See <a href="vim.host.MountInfo.md#accessible">accessible</a>.      <li> When referenced from a <a href="vim.VirtualMachine.md">VirtualMachine</a>, the target datastore           needs to be accessible from the host on which the virtual machine is           registered.  See <a href="vim.host.MountInfo.md#accessible">accessible</a>.   </ul><br>See FileInfo

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='datastore'>datastore</a> | [vim.Datastore](vim.Datastore.md "vim.Datastore") | true | System.View | Set of datastores that can be searched on this DatastoreBrowser.   <p>   The list of datastores available to browse on this DatastoreBrowser is contextual   information that depends on the object being browsed. If the host is being   browsed, the host's datastores are used. If the Datacenter is being browsed, the   Datacenter's list of datastores is used. |
| <a href='supportedType'>supportedType</a> | [vim.host.DatastoreBrowser.Query](vim.host.DatastoreBrowser.Query.md "vim.host.DatastoreBrowser.Query") | true | None | The list of supported file types. The supported file types are represented as   items in this list. For each supported file type, there is an object in the list   whose dynamic type is one of the types derived from the   <a href="vim.host.DatastoreBrowser.Query.md">FileQuery</a> data object   type. In general, the properties in this query type are not set.   <p>   Use the Query of the desired file type in the SearchSpec.query to indicate the   desired file types.   <p>   This property is used by clients to determine what kinds of file types are   supported. Clients should consult this list to avoid querying for types of virtual   machine components that are not supported. |


SearchDatastore([datastorePath](#string "string"), [searchSpec](vim.host.DatastoreBrowser.SearchSpec.md "vim.host.DatastoreBrowser.SearchSpec"))
------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | SearchDatastore |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | dynamic |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the target   datastores. The server can throw InvalidDatastorePath to indicate a malformed   datastorePath, or InaccessibleDatastore to indicate inaccessibility of the   datastore. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | vim.fault.FileFault |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the SearchSpec contains duplicate file types. |
| [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound") | if the file or folder specified by datastorePath is not   found. |




SearchDatastoreSubFolders([datastorePath](#string "string"), [searchSpec](vim.host.DatastoreBrowser.SearchSpec.md "vim.host.DatastoreBrowser.SearchSpec"))
----------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | SearchDatastoreSubFolders |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | dynamic |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the target   datastores. Typically, a specific subclass of this exception is thrown. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | vim.fault.FileFault |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the SearchSpec contains duplicate file types. |
| [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound") | if the file or folder specified by datastorePath is not   found. |




DeleteFile([datastorePath](#string "string"))
---------------------------------------------
 raises [vim.fault.CannotDeleteFile](vim.fault.CannotDeleteFile.md "vim.fault.CannotDeleteFile"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
### Deprecated
As of VI API 2.5, use <a href="vim.FileManager.md#deleteFile">DeleteDatastoreFile_Task</a>.

| service name | DeleteFile |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Datastore.DeleteFile |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the target   datastores. Typically, a specific subclass of this exception is thrown. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | vim.fault.FileFault |
| [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound") | if the file or folder specified by datastorePath is not   found. |
| [vim.fault.CannotDeleteFile](vim.fault.CannotDeleteFile.md "vim.fault.CannotDeleteFile") | if the delete operation on the file fails. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if fileInfo is not a valid FileInfo type. |




