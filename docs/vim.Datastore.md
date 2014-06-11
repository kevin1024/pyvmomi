vim.Datastore
=============
inherits from [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity")


Represents a storage location for virtual machine files. A storage location can be a   VMFS volume, a directory on Network Attached Storage, or a local file system path.   <p>   A datastore is platform-independent and host-independent. Therefore, datastores do   not change when the virtual machines they contain are moved between hosts. The scope   of a datastore is a datacenter; the datastore is uniquely named within the   datacenter.   <p>   Any reference to a virtual machine or file accessed by any host within the   datacenter must use a datastore path. A datastore path has the form   "[&lt;datastore&gt;] &lt;path&gt;", where &lt;datastore&gt; is the datastore name,   and &lt;path&gt; is a slash-delimited path from the root of the datastore. An   example datastore path is "[storage] path/to/config.vmx".   <p>   You may use the following characters in a path, but not in a datastore name:   slash (/), backslash (\), and percent (%).   <p>   All references to files in the VIM API are implicitly done using datastore paths.   <p>   When a client creates a virtual machine, it may specify the name of   the datastore, omitting the path; the system, meaning VirtualCenter or the host,   automatically assigns filenames and creates directories on the given datastore. For   example, specifying My_Datastore as a location for a virtual machine called MyVm   results in a datastore location of My_Datastore\MyVm\MyVm.vmx.   <p>   Datastores are configured per host. As part of host configuration, a HostSystem can   be configured to mount a set of network drives. Multiple hosts   may be configured to point to the same storage location. There exists only one   Datastore object per Datacenter, for each such shared location. Each Datastore   object keeps a reference to the set of hosts that have mounted the datastore. A   Datastore object can be removed only if no hosts currently have the datastore   mounted.   <p>   Thus, managing datastores is done both at the host level and the datacenter level.   Each host is configured explicitly with the set of datastores it can access. At the   datacenter, a view of the datastores across the datacenter is shown.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='info'>info</a> | [vim.Datastore.Info](vim.Datastore.Info.md "vim.Datastore.Info") | None | None | Specific information about the datastore. |
| <a href='summary'>summary</a> | [vim.Datastore.Summary](vim.Datastore.Summary.md "vim.Datastore.Summary") | None | None | Global properties of the datastore. |
| <a href='host'>host</a> | [vim.Datastore.HostMount](vim.Datastore.HostMount.md "vim.Datastore.HostMount") | true | None | Hosts attached to this datastore. |
| <a href='vm'>vm</a> | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | true | None | Virtual machines stored on this datastore. |
| <a href='browser'>browser</a> | [vim.host.DatastoreBrowser](vim.host.DatastoreBrowser.md "vim.host.DatastoreBrowser") | None | None | DatastoreBrowser used to browse this datastore. |
| <a href='capability'>capability</a> | [vim.Datastore.Capability](vim.Datastore.Capability.md "vim.Datastore.Capability") | None | None | Capabilities of this datastore. |
| <a href='iormConfiguration'>iormConfiguration</a> | [vim.StorageResourceManager.IORMConfigInfo](vim.StorageResourceManager.IORMConfigInfo.md "vim.StorageResourceManager.IORMConfigInfo") | true | None | Configuration of storage I/O resource management for the datastore.   Currently we only support storage I/O resource management on VMFS volumes   of a datastore.   <p>   This configuration may not be available if the datastore is not accessible   from any host, or if the datastore does not have VMFS volume.   The configuration can be modified using the method   <a href="vim.StorageResourceManager.md#ConfigureDatastoreIORM">ConfigureDatastoreIORM_Task</a> |


RefreshDatastore()
------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | RefreshDatastore |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the datastore or its underlying volume is not found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if unable to get the current system information           for the datastore. |




RefreshDatastoreStorageInfo()
-----------------------------

| service name | RefreshDatastoreStorageInfo |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




UpdateVirtualMachineFiles([mountPathDatastoreMapping](vim.Datastore.MountPathDatastorePair.md "vim.Datastore.MountPathDatastorePair"))
--------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.PlatformConfigFault](vim.fault.PlatformConfigFault.md "vim.fault.PlatformConfigFault"), [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | UpdateVirtualMachineFiles |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#None) |
| privilege    | Datastore.UpdateVirtualMachineFiles |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | if there exists a registered virtual machine in the volume. |
| [vim.fault.PlatformConfigFault](vim.fault.PlatformConfigFault.md "vim.fault.PlatformConfigFault") | if any error related to platform                                  occurs during the operation. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the datastore is busy, for example, while another task                             is updating the datastore after volume resignaturing                             or remounting. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed due to some error                               with the datastore; typically a specific subclass                               of the fault is reported. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if old mount path is mapped to more than one datastores,                              or if any of the datastore being mapped can not be found. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if all hosts attached to this datastore do not support                           updating virtual machine files. |




RenameDatastore([newName](#string "string"))
--------------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName")

---
### Deprecated
As of vSphere API 4.0, use <a href="vim.ManagedEntity.md#rename">Rename_Task</a>.

| service name | RenameDatastore |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Datastore.Rename |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if another datastore in this datacenter already                         has the same name. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the name is not a valid datastore name. |




DestroyDatastore()
------------------
 raises [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse")

---
### Deprecated
As of VI API 2.5 do not use this method. This method throws               <a href="vim.fault.ResourceInUse.md">ResourceInUse</a>.  Datastores are automatically               removed when no longer in use, so this method is unnecessary.

| service name | DestroyDatastore |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Datastore.Delete |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | if one or more hosts or virtual machines are configured   to use the datastore. |




DatastoreEnterMaintenanceMode()
-------------------------------
 raises [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled")

---
| service name | DatastoreEnterMaintenanceMode |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#None) |
| privilege    | Datastore.Config |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the datastore is already in maintenance mode. |
| [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled") | if the operation is canceled. |




DatastoreExitMaintenanceMode()
------------------------------
 raises [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | DatastoreExitMaintenanceMode |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#None) |
| privilege    | Datastore.Config |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the datastore is not in maintenance mode. |




