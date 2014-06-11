vim.VirtualDiskManager
======================
as of [VI API 2.5](vim.version.md#vim.version.version2)


This managed object type provides a way to manage and manipulate virtual disks   on datastores. The source and the destination names are in the form of   a URL or a datastore path.   <p>   A URL has the form   <blockquote><i>scheme</i>://<i>authority</i>/folder/<i>path</i>?dcPath=<i>dcPath</i>&dsName=<i>dsName</i></blockquote>   where   <li><i>scheme</i> is <code>http</code> or <code>https</code>.</li>   <li><i>authority</i> specifies the hostname or IP address of the VirtualCenter or   ESX server and optionally the port.</li>   <li><i>dcPath</i> is the inventory path to the Datacenter containing the    Datastore.</li>   <li><i>dsName</i> is the name of the Datastore.</li>   <li><i>path</i> is a slash-delimited path from the root of the datastore.</li>   <p>   A datastore path has the form <blockquote>[<i>datastore</i>] <i>path</i></blockquote>   where   <li><i>datastore</i> is the datastore name.</li>   <li><i>path</i> is a slash-delimited path from the root of the datastore.</li>   An example datastore path is "[storage] path/to/file.extension".   A listing of all the files, disks and folders on   a datastore can be obtained from the datastore browser.<br>See <a href="vim.host.DatastoreBrowser.md">HostDatastoreBrowser</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


CreateVirtualDisk([name](#string "string"), [datacenter](vim.Datacenter.md "vim.Datacenter"), [spec](vim.VirtualDiskManager.VirtualDiskSpec.md "vim.VirtualDiskManager.VirtualDiskSpec"))
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore")

---
| service name | CreateVirtualDisk |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if an error occurs creating the virtual disk. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the datastore. |




DeleteVirtualDisk([name](#string "string"), [datacenter](vim.Datacenter.md "vim.Datacenter"))
---------------------------------------------------------------------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore")

---
| service name | DeleteVirtualDisk |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if an error occurs deleting the virtual disk. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the datastore. |




MoveVirtualDisk([sourceName](#string "string"), [sourceDatacenter](vim.Datacenter.md "vim.Datacenter"), [destName](#string "string"), [destDatacenter](vim.Datacenter.md "vim.Datacenter"), [profile](vim.vm.ProfileSpec.md "vim.vm.ProfileSpec"))
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore")

---
| service name | MoveVirtualDisk |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if an error occurs renaming the virtual disk. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the source   or destination datastore. |




CopyVirtualDisk([sourceName](#string "string"), [sourceDatacenter](vim.Datacenter.md "vim.Datacenter"), [destName](#string "string"), [destDatacenter](vim.Datacenter.md "vim.Datacenter"), [destSpec](vim.VirtualDiskManager.VirtualDiskSpec.md "vim.VirtualDiskManager.VirtualDiskSpec"))
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.InvalidDiskFormat](vim.fault.InvalidDiskFormat.md "vim.fault.InvalidDiskFormat")

---
| service name | CopyVirtualDisk |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if an error occurs cloning the virtual disk. |
| [vim.fault.InvalidDiskFormat](vim.fault.InvalidDiskFormat.md "vim.fault.InvalidDiskFormat") | if the destination's format is not supported. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the source                            or destination datastore. |




ExtendVirtualDisk([name](#string "string"), [datacenter](vim.Datacenter.md "vim.Datacenter"))
---------------------------------------------------------------------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore")

---
| service name | ExtendVirtualDisk |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if an error occurs extending the virtual disk. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the datastore. |




QueryVirtualDiskFragmentation([name](#string "string"), [datacenter](vim.Datacenter.md "vim.Datacenter"))
---------------------------------------------------------------------------------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore")

---
| service name | QueryVirtualDiskFragmentation |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type | None |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if an error occurs reading the virtual disk. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the datastore. |




DefragmentVirtualDisk([name](#string "string"), [datacenter](vim.Datacenter.md "vim.Datacenter"))
-------------------------------------------------------------------------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore")

---
| service name | DefragmentVirtualDisk |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if an error occurs defragmenting the virtual disk. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the datastore. |




ShrinkVirtualDisk([name](#string "string"), [datacenter](vim.Datacenter.md "vim.Datacenter"))
---------------------------------------------------------------------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore")

---
| service name | ShrinkVirtualDisk |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if an error occurs shrinking the virtual disk. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the datastore. |




InflateVirtualDisk([name](#string "string"), [datacenter](vim.Datacenter.md "vim.Datacenter"))
----------------------------------------------------------------------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore")

---
| service name | InflateVirtualDisk |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if an error occurs inflating the virtual disk. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the datastore. |




EagerZeroVirtualDisk([name](#string "string"), [datacenter](vim.Datacenter.md "vim.Datacenter"))
------------------------------------------------------------------------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore")

---
| service name | EagerZeroVirtualDisk |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if an error occurs while eager-zeroing the virtual disk. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the datastore. |




ZeroFillVirtualDisk([name](#string "string"), [datacenter](vim.Datacenter.md "vim.Datacenter"))
-----------------------------------------------------------------------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore")

---
| service name | ZeroFillVirtualDisk |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if an error occurs zero filling the virtual disk. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the datastore. |




SetVirtualDiskUuid([name](#string "string"), [datacenter](vim.Datacenter.md "vim.Datacenter"), [uuid](#string "string"))
------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore")

---
| service name | SetVirtualDiskUuid |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if an error occurs updating the virtual disk. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the datastore. |




QueryVirtualDiskUuid([name](#string "string"), [datacenter](vim.Datacenter.md "vim.Datacenter"))
------------------------------------------------------------------------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore")

---
| service name | QueryVirtualDiskUuid |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if an error occurs reading the virtual disk. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the datastore. |




QueryVirtualDiskGeometry([name](#string "string"), [datacenter](vim.Datacenter.md "vim.Datacenter"))
----------------------------------------------------------------------------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore")

---
| service name | QueryVirtualDiskGeometry |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if an error occurs reading the virtual disk. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the datastore. |




