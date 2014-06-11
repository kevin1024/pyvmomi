vim.ResourcePool
================
inherits from [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity")


Represents a set of physical resources: a single host,   a subset of a host's resources, or resources spanning multiple hosts.   Resource pools can be subdivided by creating child resource pools. In   order to run, a virtual machine must be associated as a child of a resource   pool.   <p>   In a parent/child hierarchy of resource pools and virtual machines, the   single resource pool that has no parent pool is known as the <em>root resource   pool</em>.   <p>   <b>Configuration</b>   <p>   A resource pool is configured with a set of CPU (in MHz) and memory (in MB)   resources. These resources are specified in absolute terms with a resource   reservation and a resource limit, along with a shares setting. The shares   are used during resource contention, to ensure graceful degradation.   <p>   For the root resource pool, the values of the reservation and   the limit are set by the system and are not configurable. The   reservation and limit are set to the same value, indicating the total amount   of resources the system has available to run virtual machines. This is   computed as the aggregated CPU and memory resources provided by the set   of current available hosts in the parent compute resource minus the   overhead of the virtualization layer.   <p>   Since the resource pool configuration is absolute (in MHz or MB), the   configuration can become invalid when resources are removed.  This can   happen if a host is removed from the cluster, if a host becomes   unavailable, or if a host is placed in maintenance mode. When this   happens, the system flags misconfigured resource pools and displays the   reservations and limits that are in effect. Further, in a DRS enabled cluster,   the tree can be misconfigured if the user bypasses VirtualCenter and powers on   VMs directly on the host.   <p>   <b>A General Discussion of Resource pool states and admission control</b>    There are three states that the resource pool tree can be in: undercommited   (green), overcommited (yellow), and inconsistent (red). Depending on the   state, different resource pool configuration policies are enforced. The   states are described in more detail below:   <ul>   <li> <strong>GREEN (aka undercommitted)</strong>: We have a tree that is   in a <em>good</em> state. Every node has a reservation greater than the sum of   the reservations for its children. We have enough capacity at the root to   satisfy all the resources reserved by the children. All operations   performed on the tree, such as powering on virtual machines, creating   new resource pools, or reconfiguring resource settings, will ensure   that the above constraints are maintained. </li>    <li> <strong>RED (aka. inconsistent)</strong>: One or more nodes in the   tree has children whose reservations are greater than the node is configured to   support. For example, i) a resource pool with a fixed reservation has a running   virtual machine with a reservation that is higher than the reservation on   resource pool itself., or ii) the child reservations are greater than the limit.   <p>   In this state, the DRS algorithm is disabled until the resource pool tree's   configuration has  been brought back into a consistent state. We also restrict   the resources that such invalid nodes request from their parents to the   configured reservation/limit, in an attempt to isolate the problem to a small   subtree. For the rest of the tree, we determine whether the cluster is   undercommitted or overcommitted according to the existing rules and perform   admission control accordingly.   <p>   Note that since all changes to the resource settings are validated on the   VirtualCenter server, the system cannot be brought into this state by simply   manipulating a cluster resource pool tree through  VirtualCenter. It can only   happen if a virtual machine gets powered on directly on a host that is part of   a DRS cluster.   </li>    <li> <strong>YELLOW (aka overcommitted)</strong>: In this state, the tree is   consistent internally, but the root resource pool does not have the capacity at   to meet the reservation of its children. We can only go from GREEN -&gt; YELLOW if   we lose resources at the root. For example, hosts becomes unavailable or is   put into maintenance mode. Note that we will always have enough capacity at the root   to run all currently powered on VMs. However, we may not be able to satisfy all   resource pool reservations in the tree. In this state, the reservation configured for   a resource pool is no longer guaranteed, but the limits are still enforced.   This provides additional flexibility for bringing the tree back into a   consistent state, without risking bringing the tree into a RED state. In   more detail:   <ul>   <li> <strong>Resource Pool</strong> The root is considered to have unlimited   capacity. You can reserve resources without any check except the   requirement that the tree remains consistent. This means that   nodes whose parents are all configured with expandable reservations and no limit   will have unlimited available resources. However, if there is an ancestor with   a fixed reservation or an expandable reservation with a limit somewhere, then the   node will be limited by the reservation/limit of the ancestor.   </li>   <li> <strong>Virtual Machine</strong> Virtual machines are limited by ancestors   with a fixed reservation and the capacity at the root.   </li>   </ul>   </li>   </ul>    <p>   <b>Destroying a ResourcePool</b>   <p>   When a ResourcePool is destroyed, all the virtual machines are reassigned to its   parent pool. The root resource pool cannot be destroyed, and invoking destroy   on it will throw an InvalidType fault.   <p>   Any vApps in the ResourcePool will be moved to the ResourcePool's parent   before the pool is destroyed.   <p>   The Resource.DeletePool privilege must be held on the pool as well as the parent   of the resource pool.  Also, the Resource.AssignVMToPool privilege must be held   on the resource pool's parent pool and any virtual machines that are reassigned.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='summary'>summary</a> | [vim.ResourcePool.Summary](vim.ResourcePool.Summary.md "vim.ResourcePool.Summary") | None | None | Basic information about a resource pool.    In releases after vSphere API 5.0, vSphere Servers might not   generate property collector update notifications for this property.   To obtain the latest value of the property, you can use   PropertyCollector methods RetrievePropertiesEx or WaitForUpdatesEx.   If you use the PropertyCollector.WaitForUpdatesEx method, specify   an empty string for the version parameter. Any other version value will not   produce any property values as no updates are generated. |
| <a href='runtime'>runtime</a> | [vim.ResourcePool.RuntimeInfo](vim.ResourcePool.RuntimeInfo.md "vim.ResourcePool.RuntimeInfo") | None | None | Runtime information about a resource pool.   The <a href="vim.ResourcePool.ResourceUsage.md">ResourcePoolResourceUsage</a> information within   <a href="vim.ResourcePool.RuntimeInfo.md">ResourcePoolRuntimeInfo</a> can be transiently stale.   Use <a href="vim.ResourcePool.md#refreshRuntime">RefreshRuntime</a> method to   update the information.    In releases after vSphere API 5.0, vSphere Servers might not   generate property collector update notifications for this property.   To obtain the latest value of the property, you can use   PropertyCollector methods RetrievePropertiesEx or WaitForUpdatesEx.   If you use the PropertyCollector.WaitForUpdatesEx method, specify   an empty string for the version parameter. Any other version value will not   produce any property values as no updates are generated. |
| <a href='owner'>owner</a> | [vim.ComputeResource](vim.ComputeResource.md "vim.ComputeResource") | None | System.View | The ComputeResource to which this set of one or more nested resource pools   belong. |
| <a href='resourcePool'>resourcePool</a> | [vim.ResourcePool](vim.ResourcePool.md "vim.ResourcePool") | true | System.View | The set of child resource pools. |
| <a href='vm'>vm</a> | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | true | System.View | The set of virtual machines associated with this resource pool. |
| <a href='config'>config</a> | [vim.ResourceConfigSpec](vim.ResourceConfigSpec.md "vim.ResourceConfigSpec") | None | None | Configuration of this resource pool. |
| <a href='childConfiguration'>childConfiguration</a> | [vim.ResourceConfigSpec](vim.ResourceConfigSpec.md "vim.ResourceConfigSpec") | true | None | The resource configuration of all direct children (VirtualMachine and   ResourcePool) of this resource group. |


UpdateConfig([name](#string "string"), [config](vim.ResourceConfigSpec.md "vim.ResourceConfigSpec"))
----------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess"), [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | UpdateConfig |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | dynamic |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the name is not a valid entity name. |
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if the name is changed to an already existing name. |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | if the pool specification cannot be    supported by the parent resource pool or vApp. |
| [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess") | if the changeVersion does not match the server's    changeVersion for the configuration. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the parameters are out of range,    or if the reservationLimit field is set. |




MoveIntoResourcePool([list](vim.ManagedEntity.md "vim.ManagedEntity"))
----------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName")

---
| service name | MoveIntoResourcePool |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | dynamic |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if this pool already contains an object with              the given name. |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | if the move would violate the resource usage   policy. Typically, a more specific subclass, such as   InsufficientMemoryResourcesFault. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if an ancestor of this pool is in the list. |




UpdateChildResourceConfiguration([spec](vim.ResourceConfigSpec.md "vim.ResourceConfigSpec"))
--------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | UpdateChildResourceConfiguration |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | dynamic |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | vim.fault.InvalidState |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | if the operation would violate a resource   usage policy. Typically, a more specific subclass, such as   InsufficientMemoryResourcesFault will be thrown. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if a managed entity that is not a child of this group                           is included. |




CreateResourcePool([name](#string "string"), [spec](vim.ResourceConfigSpec.md "vim.ResourceConfigSpec"))
--------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | CreateResourcePool |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Resource.CreatePool |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the name is not a valid entity name. |
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if this pool already contains an object   with the given name. |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | if the operation would violate a resource   usage policy. Typically, a more specific subclass, such as   InsufficientCpuResourcesFault will be thrown. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the ComputeResource does not support   nested resource pools. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the pool specification is invalid. |




DestroyChildren()
-----------------

| service name | DestroyChildren |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | dynamic |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




CreateVApp([name](#string "string"), [resSpec](vim.ResourceConfigSpec.md "vim.ResourceConfigSpec"), [configSpec](vim.vApp.VAppConfigSpec.md "vim.vApp.VAppConfigSpec"), [vmFolder](vim.Folder.md "vim.Folder"))
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | CreateVApp |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | VApp.Create |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the name is not a valid entity name. |
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if this pool already contains an object   with the given name. |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | if the operation would violate a resource   usage policy. Typically, a more specific subclass, such as   InsufficientCpuResourcesFault will be thrown. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the resource pool does not support the operation in   its current state. This will typically be a subclass such   as <a href="vim.fault.NoActiveHostInCluster.md">NoActiveHostInCluster</a>. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | or a more specific subclass, if errors are found in                       the supplied in VApp configuration. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the ComputeResource does not support   nested resource pools. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the pool specification is invalid. |




CreateChildVM([config](vim.vm.ConfigSpec.md "vim.vm.ConfigSpec"), [host](vim.HostSystem.md "vim.HostSystem"))
-------------------------------------------------------------------------------------------------------------
 raises [vim.fault.OutOfBounds](vim.fault.OutOfBounds.md "vim.fault.OutOfBounds"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.VmWwnConflict](vim.fault.VmWwnConflict.md "vim.fault.VmWwnConflict"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.FileAlreadyExists](vim.fault.FileAlreadyExists.md "vim.fault.FileAlreadyExists"), [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault")

---
| service name | CreateChildVM |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | VirtualMachine.Inventory.Create |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if the configSpec has incorrect values. Typically, a more           specific subclass is thrown. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a problem creating the virtual machine on disk.           Typically, a more specific subclass, such as NoDiskSpace, will be thrown. |
| [vim.fault.OutOfBounds](vim.fault.OutOfBounds.md "vim.fault.OutOfBounds") | if Host.capability.maxSupportedVMs is exceeded. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the name is not a valid entity name. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the           target datastores. |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | if this operation would violate a resource           usage policy. |
| [vim.fault.FileAlreadyExists](vim.fault.FileAlreadyExists.md "vim.fault.FileAlreadyExists") | if the requested cfgPath for the virtual machine's           configuration file already exists. |
| [vim.fault.VmWwnConflict](vim.fault.VmWwnConflict.md "vim.fault.VmWwnConflict") | if the WWN of the virtual machine has been used by           other virtual machines. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if this resource pool is not a vApp or is a child           of a vApp. |




RegisterChildVM([path](#string "string"), [name](#string "string"), [host](vim.HostSystem.md "vim.HostSystem"))
---------------------------------------------------------------------------------------------------------------
 raises [vim.fault.OutOfBounds](vim.fault.OutOfBounds.md "vim.fault.OutOfBounds"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault")

---
| service name | RegisterChildVM |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | VirtualMachine.Inventory.Register |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.OutOfBounds](vim.fault.OutOfBounds.md "vim.fault.OutOfBounds") | if the maximum number of VMs has been exceeded. |
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | if the virtual machine is already registered. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the           target datastores. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the configuration file is not found on the system. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the entity name is invalid. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if the format / configuration of the virtual machine           is invalid. Typically, a more specific fault is thrown such as           InvalidFormat if the configuration file cannot be read, or           InvalidDiskFormat if the disks cannot be read. |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | if this operation would violate a resource           usage policy. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is an error accessing the files on disk. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the operation is not supported. For example, if the           operation is invoked on a resource pool that is unrelated to a vApp. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if any of the arguments are invalid and a more specific           fault type does not apply. |




ImportVApp([spec](vim.ImportSpec.md "vim.ImportSpec"), [folder](vim.Folder.md "vim.Folder"), [host](vim.HostSystem.md "vim.HostSystem"))
----------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.OutOfBounds](vim.fault.OutOfBounds.md "vim.fault.OutOfBounds"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.VmWwnConflict](vim.fault.VmWwnConflict.md "vim.fault.VmWwnConflict"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vim.fault.FileAlreadyExists](vim.fault.FileAlreadyExists.md "vim.fault.FileAlreadyExists"), [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | ImportVApp |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | VApp.Import |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if a VM configSpec has incorrect values. Typically, a more           specific subclass is thrown. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a problem creating the virtual machine on disk.           Typically, a more specific subclass, such as NoDiskSpace, will be thrown. |
| [vim.fault.OutOfBounds](vim.fault.OutOfBounds.md "vim.fault.OutOfBounds") | if Host.capability.maxSupportedVMs is exceeded. |
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if another virtual machine in the same folder already has           the specified target name. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the name is not a valid entity name. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the           target datastores. |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | if this operation would violate a resource           usage policy. |
| [vim.fault.FileAlreadyExists](vim.fault.FileAlreadyExists.md "vim.fault.FileAlreadyExists") | if the requested cfgPath for the virtual machine's           configuration file already exists. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the virtual machine is being created within a folder           whose <a href="vim.Folder.md#childType">childType</a> property is not set to "VirtualMachine",           a vApp is being imported into a resource pool that does not support           nested resource pools, or a virtual machine is being imported into a resource           pool and no folder is given. |
| [vim.fault.VmWwnConflict](vim.fault.VmWwnConflict.md "vim.fault.VmWwnConflict") | if the WWN of the virtual machine has been used by           other virtual machines. |




QueryResourceConfigOption()
---------------------------

| service name | QueryResourceConfigOption |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#None) |
| privilege    | Resource.EditPool |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




RefreshRuntime()
----------------

| service name | RefreshRuntime |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




