vim.Folder
==========
inherits from [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity")


The <a href="vim.Folder.md">Folder</a> managed object is a container for storing and organizing   inventory objects. Folders can contain folders and other objects.   The <a href="vim.Folder.md#childType">childType</a> property identifies a folder's type   and determines the types of folders and objects the folder can contain.   <ul>       <li> A folder can contain a child folder of the same type as the parent folder.       <li> All <a href="vim.Datacenter.md">Datacenter</a> objects contain dedicated folders for:       <ul type="SQUARE">           <li> <a href="vim.VirtualMachine.md">VirtualMachine</a>, templates, and <a href="vim.VirtualApp.md">VirtualApp</a> objects.           <li> <a href="vim.ComputeResource.md">ComputeResource</a> hierarchies.           <li> <a href="vim.Network.md">Network</a>, <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>, and                 <a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a> objects.           <li> <a href="vim.Datastore.md">Datastore</a> objects.       </ul>       <li> A folder can contain child objects of type <a href="vim.Folder.md#childType">childType</a>.             Virtual machine and network entity folders can also contain additional object types.       <li> The root folder is a data center folder.   </ul>   See <a href="vim.ServiceInstance.md">ServiceInstance</a> for a representation of the organization of the inventory.   <p>   The <a href="vim.Folder.md">Folder</a> managed object also acts as a factory object, meaning it   creates new entities in a folder. The object provides methods to create   child folders and objects, methods to add existing objects to folders, and   methods to remove objects from folders and to delete folders.   <p>   <a href="vim.Folder.md">Folder</a> inherits the <a href="vim.ManagedEntity.md#destroy">Destroy_Task</a> method.   <a href="vim.ManagedEntity.md#destroy">Destroy_Task</a> is a recursive operation that removes all child objects and   folders. When you call <a href="vim.ManagedEntity.md#destroy">Destroy_Task</a> to destroy a folder, the system uses   the specified folder as a root and traverses its descendant hierarchy, calling    <a href="vim.ManagedEntity.md#destroy">Destroy_Task</a> on each object.   <a href="vim.ManagedEntity.md#destroy">Destroy_Task</a> is a single operation that treats each recursive call as a   single transaction, committing each call to remove an object individually.   If <a href="vim.ManagedEntity.md#destroy">Destroy_Task</a> fails on an object, the method terminates at that point   with an exception, leaving some or all of the objects still in the inventory.   <p>    Notes on the folder destroy method:   <ul>       <li>Calling <a href="vim.ManagedEntity.md#destroy">Destroy_Task</a> on a virtual machine folder recursively calls        <a href="vim.ManagedEntity.md#destroy">Destroy_Task</a> on all the child virtual machines and vApps, which are then       removed from disk.       Use <a href="vim.Folder.md#unregisterAndDestroy">UnregisterAndDestroy_Task</a>       to unregister virtual machines or vApps recursively without       removing them from the disk.       <li>For virtual machine folders, the <a href="vim.ManagedEntity.md#destroy">Destroy_Task</a> method requires the       VirtualMachine.Delete privilege on the folder as well as        all virtual machines to be destroyed. It also requires the VirtualApp.Delete       privilege on all VirtualApp objects to be destroyed.       <li>Destroying a host folder or datacenter folder unregisters all child hosts       and virtual machines from vCenter. The hosts are simply removed       from the inventory, along with their virtual machines. The virtual machines       are not removed from disk nor are their runtime states changed.       <li> You can remove network and datastore folders only if they are empty.       <li> You cannot destroy, rename, or move the virtual machine, compute resource,            network entity, and datastore child folders of a Datacenter.   </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='childType'>childType</a> | string | true | System.View | Specifies the object types a folder may contain.    When you create a folder, it inherits its childType from the parent folder   in which it is created. childType is an array of strings. Each array entry    identifies a set of object types - Folder and one or more managed object   types. The following list shows childType values for the different folders:   <ul>       <li> { "vim.Folder", "vim.Datacenter" } - Identifies the root folder            and its descendant folders. Data center folders can contain            child data center folders and Datacenter managed objects.            Datacenter objects contain virtual machine, compute resource,            network entity, and datastore folders.</li>       <li> { "vim.Folder", "vim.Virtualmachine", "vim.VirtualApp" } - Identifies            a virtual machine folder. A virtual machine folder may contain child            virtual machine folders. It also can contain VirtualMachine managed objects,             templates, and VirtualApp managed objects.</li>       <li> { "vim.Folder", "vim.ComputeResource" } - Identifies a             compute resource folder, which contains child compute resource folders            and ComputeResource hierarchies.</li>       <li> { "vim.Folder", "vim.Network" } - Identifies a network entity folder.            Network entity folders on a vCenter Server can contain Network,            DistributedVirtualSwitch, and DistributedVirtualPortgroup managed            objects. Network entity folders on an ESXi host can contain only            Network objects.</li>       <li> { "vim.Folder", "vim.Datastore" } - Identifies a datastore folder.            Datastore folders can contain child datastore folders and Datastore            managed objects.</li>   </ul> |
| <a href='childEntity'>childEntity</a> | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | true | System.View | An array of managed object references. Each entry is a reference to a child entity. |


CreateFolder([name](#string "string"))
--------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName")

---
| service name | CreateFolder |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Folder.Create |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if another object in the same folder has the target name. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the name is not a valid entity name. |




MoveIntoFolder([list](vim.ManagedEntity.md "vim.ManagedEntity"))
----------------------------------------------------------------
 raises [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vim.fault.InvalidFolder](vim.fault.InvalidFolder.md "vim.fault.InvalidFolder"), [vim.fault.DisallowedOperationOnFailoverHost](vim.fault.DisallowedOperationOnFailoverHost.md "vim.fault.DisallowedOperationOnFailoverHost"), [vim.fault.VmAlreadyExistsInDatacenter](vim.fault.VmAlreadyExistsInDatacenter.md "vim.fault.VmAlreadyExistsInDatacenter"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | MoveIntoFolder |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | dynamic |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if this folder already contains an object with              the specified name. |
| [vim.fault.InvalidFolder](vim.fault.InvalidFolder.md "vim.fault.InvalidFolder") | if a Folder that is a parent of this Folder is part              of the list of objects. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if a HostSystem is not part of the same              datacenter, not part of a ClusterComputeResource, or not in              maintenance mode. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the entity is being moved into a folder           whose <a href="vim.Folder.md#childType">childType</a> property is not set to           the appropriate value.  For example, a VirtualMachine entity           cannot be moved into a folder whose ChildType property value           does not contain "VirtualMachine". |
| [vim.fault.DisallowedOperationOnFailoverHost](vim.fault.DisallowedOperationOnFailoverHost.md "vim.fault.DisallowedOperationOnFailoverHost") | if the host is being moved           out of a cluster and was configured as a failover host in that           cluster. See <a href="vim.cluster.FailoverHostAdmissionControlPolicy.md">ClusterFailoverHostAdmissionControlPolicy</a>. |
| [vim.fault.VmAlreadyExistsInDatacenter](vim.fault.VmAlreadyExistsInDatacenter.md "vim.fault.VmAlreadyExistsInDatacenter") | if moving a standalone host between           datacenters, and one or more of the host's virtual machines is           already registered to a host in the destination datacenter. |




CreateVM([config](vim.vm.ConfigSpec.md "vim.vm.ConfigSpec"), [pool](vim.ResourcePool.md "vim.ResourcePool"), [host](vim.HostSystem.md "vim.HostSystem"))
--------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.OutOfBounds](vim.fault.OutOfBounds.md "vim.fault.OutOfBounds"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.VmWwnConflict](vim.fault.VmWwnConflict.md "vim.fault.VmWwnConflict"), [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vim.fault.FileAlreadyExists](vim.fault.FileAlreadyExists.md "vim.fault.FileAlreadyExists"), [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | CreateVM |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Inventory.Create |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if the configSpec has incorrect values. Typically, a more           specific subclass is thrown. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a problem creating the virtual machine on disk.           Typically, a more specific subclass, such as NoDiskSpace, will be thrown. |
| [vim.fault.OutOfBounds](vim.fault.OutOfBounds.md "vim.fault.OutOfBounds") | if Host.capability.maxSupportedVMs is exceeded. |
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if another virtual machine in the same folder already has           the specified target name. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the name is not a valid entity name. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the           target datastores. |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | if this operation would violate a resource           usage policy. |
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | if the requested cfgPath (or the default cfgPath)           for the virtual machine's configuration file is already loaded           in the inventory. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation is not allowed in current state of           the entities involved. |
| [vim.fault.FileAlreadyExists](vim.fault.FileAlreadyExists.md "vim.fault.FileAlreadyExists") | if the requested cfgPath for the virtual machine's           configuration file already exists. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the virtual machine is being created within a folder           whose <a href="vim.Folder.md#childType">childType</a> property is not set to           "VirtualMachine". |
| [vim.fault.VmWwnConflict](vim.fault.VmWwnConflict.md "vim.fault.VmWwnConflict") | if the WWN of the virtual machine has been used by           other virtual machines. |




RegisterVM([path](#string "string"), [name](#string "string"), [pool](vim.ResourcePool.md "vim.ResourcePool"), [host](vim.HostSystem.md "vim.HostSystem"))
----------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.OutOfBounds](vim.fault.OutOfBounds.md "vim.fault.OutOfBounds"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | RegisterVM |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Inventory.Register |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.OutOfBounds](vim.fault.OutOfBounds.md "vim.fault.OutOfBounds") | if the maximum number of VMs for this folder has been           exceeded. The maximum number is determined by           Host.capability.maxSupportedVMs. |
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if another virtual machine in the same folder has           the target name. |
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | if the virtual machine is already registered. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the           target datastores. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the configuration file is not found on the system. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the entity name is invalid. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if the format / configuration of the virtual machine           is invalid. Typically, a more specific fault is thrown such as           InvalidFormat if the configuration file cannot be read, or           InvalidDiskFormat if the disks cannot be read. |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | if this operation would violate a resource           usage policy. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is an error accessing the files on disk. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation is not allowed in current state of           the entities involved. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the operation is not supported. For example,           templates are not supported directly on hosts. Also, if the operation           is invoked on a folder whose <a href="vim.Folder.md#childType">childType</a> property is           not set to "VirtualMachine". |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if any of the arguments such as host or resource pool           are not set to valid values. |




CreateCluster([name](#string "string"), [spec](vim.cluster.ConfigSpec.md "vim.cluster.ConfigSpec"))
---------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
### Deprecated
As of VI API 2.5, use <a href="vim.Folder.md#createClusterEx">CreateClusterEx</a>.

| service name | CreateCluster |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Inventory.CreateCluster |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if an entity with that name already exists. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the name is not a valid entity name. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the cluster configuration specification parameter is           invalid. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the cluster is being added to a folder whose           <a href="vim.Folder.md#childType">childType</a> property value does not contain           "ComputeResource" or "ClusterComputeResource". |




CreateClusterEx([name](#string "string"), [spec](vim.cluster.ConfigSpecEx.md "vim.cluster.ConfigSpecEx"))
---------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | CreateClusterEx |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | Host.Inventory.CreateCluster |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if an entity with that name already exists. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the name is not a valid entity name. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the cluster configuration specification parameter is           invalid. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the cluster is being added to a folder whose           <a href="vim.Folder.md#childType">childType</a> property value does not contain           "ComputeResource" or "ClusterComputeResource". |




AddStandaloneHost([spec](vim.host.ConnectSpec.md "vim.host.ConnectSpec"), [compResSpec](vim.ComputeResource.ConfigSpec.md "vim.ComputeResource.ConfigSpec"), [license](#string "string"))
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.SSLVerifyFault](vim.fault.SSLVerifyFault.md "vim.fault.SSLVerifyFault"), [vim.fault.AgentInstallFailed](vim.fault.AgentInstallFailed.md "vim.fault.AgentInstallFailed"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConnectFault](vim.fault.HostConnectFault.md "vim.fault.HostConnectFault"), [vim.fault.NoHost](vim.fault.NoHost.md "vim.fault.NoHost"), [vim.fault.AlreadyBeingManaged](vim.fault.AlreadyBeingManaged.md "vim.fault.AlreadyBeingManaged"), [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vim.fault.AlreadyConnected](vim.fault.AlreadyConnected.md "vim.fault.AlreadyConnected"), [vim.fault.NotSupportedHost](vim.fault.NotSupportedHost.md "vim.fault.NotSupportedHost"), [vmodl.fault.NotEnoughLicenses](vmodl.fault.NotEnoughLicenses.md "vmodl.fault.NotEnoughLicenses"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | AddStandaloneHost |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Inventory.AddStandaloneHost |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin") | if authentication with the host fails. |
| [vim.fault.HostConnectFault](vim.fault.HostConnectFault.md "vim.fault.HostConnectFault") | if an error occurred when attempting to connect 		   to a host. Typically, a more specific subclass, such as 		   AlreadyBeingManaged, is thrown. |
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if another host in the same folder has the name. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if an argument is specified incorrectly. |
| [vim.fault.AlreadyBeingManaged](vim.fault.AlreadyBeingManaged.md "vim.fault.AlreadyBeingManaged") | if the host is already being managed by a           vCenter server. If the host is being managed by a different           vCenter server, this can be overridden by the "force" flag in the           connection specification. |
| [vmodl.fault.NotEnoughLicenses](vmodl.fault.NotEnoughLicenses.md "vmodl.fault.NotEnoughLicenses") | if there are not enough licenses to add the host. |
| [vim.fault.NoHost](vim.fault.NoHost.md "vim.fault.NoHost") | if the host cannot be contacted. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is being added to a folder whose           <a href="vim.Folder.md#childType">childType</a> property does not contain           "ComputeResource". |
| [vim.fault.NotSupportedHost](vim.fault.NotSupportedHost.md "vim.fault.NotSupportedHost") | if the host is running a software version that is not                            supported. |
| [vim.fault.AgentInstallFailed](vim.fault.AgentInstallFailed.md "vim.fault.AgentInstallFailed") | if there is an error installing the vCenter           agent on the new host. |
| [vim.fault.AlreadyConnected](vim.fault.AlreadyConnected.md "vim.fault.AlreadyConnected") | if addConnected is true and the host is already           connected to vCenter. |
| [vim.fault.SSLVerifyFault](vim.fault.SSLVerifyFault.md "vim.fault.SSLVerifyFault") | if the host certificate could not be authenticated |




CreateDatacenter([name](#string "string"))
------------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | CreateDatacenter |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Datacenter.Create |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if an entity with that name already exists. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the new name is not a valid entity name. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the datacenter is being created within a folder whose           <a href="vim.Folder.md#childType">childType</a> property value does not contain           "Datacenter". |




UnregisterAndDestroy()
----------------------
 raises [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | UnregisterAndDestroy |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Folder.Delete |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess") | if another client modifies the folder contents           before this operation completes. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if a virtual machine is not powered off or suspended. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the <a href="vim.Folder.md#childType">childType</a> property of the           folder is not set to "VirtualMachine". |




CreateDVS([spec](vim.DistributedVirtualSwitch.CreateSpec.md "vim.DistributedVirtualSwitch.CreateSpec"))
-------------------------------------------------------------------------------------------------------
 raises [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound"), [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault")

---
| service name | CreateDVS |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | DVSwitch.Create |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | vim.fault.DvsFault |
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | vim.fault.DuplicateName |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | vim.fault.InvalidName |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | vim.fault.NotFound |
| [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized") | if login-session's extension key does not match           (<a href="vim.DistributedVirtualSwitch.ConfigInfo.md#extensionKey">extensionKey</a>). |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if called directly on a host. |




CreateStoragePod([name](#string "string"))
------------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | CreateStoragePod |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#None) |
| privilege    | Folder.Create |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if an entity with that name already exists. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the name is not a valid entity name. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the storage pod is being added to a folder whose           <a href="vim.Folder.md#childType">childType</a> property value does not contain           "StoragePod".  <p> |




