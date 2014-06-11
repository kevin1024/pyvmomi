vim.VirtualMachine
==================
inherits from [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity")


VirtualMachine is the managed object type for manipulating virtual machines,   including templates that can be deployed (repeatedly) as new virtual machines.   This type provides methods for configuring and controlling a virtual machine.   <p>   VirtualMachine extends the ManagedEntity type because virtual machines are   part of a virtual infrastructure inventory. The parent of a virtual machine   must be a folder, and a virtual machine has no children.   <p>   Destroying a virtual machine disposes of all associated storage, including   the virtual disks. To remove a virtual machine while retaining its   virtual disk storage, a client must remove the virtual disks   from the virtual machine before destroying it.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='capability'>capability</a> | [vim.vm.Capability](vim.vm.Capability.md "vim.vm.Capability") | None | None | Information about the runtime capabilities of this virtual machine. |
| <a href='config'>config</a> | [vim.vm.ConfigInfo](vim.vm.ConfigInfo.md "vim.vm.ConfigInfo") | true | None | Configuration of this virtual machine, including the name and UUID.   <p>   This property is set when a virtual machine is created or when   the <a href="vim.VirtualMachine.md#reconfigure">reconfigVM</a> method is called.   <p>   The virtual machine configuration is not guaranteed to be available.   For example, the configuration information would be unavailable   if the server is unable to access the virtual machine files on disk,   and is often also unavailable during the initial phases of   virtual machine creation. |
| <a href='layout'>layout</a> | [vim.vm.FileLayout](vim.vm.FileLayout.md "vim.vm.FileLayout") | true | None | Detailed information about the files that comprise this virtual machine.   <p> |
| <a href='layoutEx'>layoutEx</a> | [vim.vm.FileLayoutEx](vim.vm.FileLayoutEx.md "vim.vm.FileLayoutEx") | true | None | Detailed information about the files that comprise this virtual machine.   <p>   Can be explicitly refreshed by the <a href="vim.VirtualMachine.md#refreshStorageInfo">RefreshStorageInfo</a> operation.    In releases after vSphere API 5.0, vSphere Servers might not   generate property collector update notifications for this property.   To obtain the latest value of the property, you can use   PropertyCollector methods RetrievePropertiesEx or WaitForUpdatesEx.   If you use the PropertyCollector.WaitForUpdatesEx method, specify   an empty string for the version parameter. Any other version value will not   produce any property values as no updates are generated. |
| <a href='storage'>storage</a> | [vim.vm.StorageInfo](vim.vm.StorageInfo.md "vim.vm.StorageInfo") | true | None | Storage space used by the virtual machine, split by datastore.   Can be explicitly refreshed by the <a href="vim.VirtualMachine.md#refreshStorageInfo">RefreshStorageInfo</a> operation.    In releases after vSphere API 5.0, vSphere Servers might not   generate property collector update notifications for this property.   To obtain the latest value of the property, you can use   PropertyCollector methods RetrievePropertiesEx or WaitForUpdatesEx.   If you use the PropertyCollector.WaitForUpdatesEx method, specify   an empty string for the version parameter. Any other version value will not   produce any property values as no updates are generated. |
| <a href='environmentBrowser'>environmentBrowser</a> | [vim.EnvironmentBrowser](vim.EnvironmentBrowser.md "vim.EnvironmentBrowser") | None | None | The current virtual machine's environment browser object. This contains  information on all the configurations that can be used on the  virtual machine. This is identical to the environment browser on  the <a href="vim.ComputeResource.md">ComputeResource</a> to which this virtual machine belongs. |
| <a href='resourcePool'>resourcePool</a> | [vim.ResourcePool](vim.ResourcePool.md "vim.ResourcePool") | true | None | The current resource pool that specifies resource allocation  for this virtual machine.  <p>  This property is set when a virtual machine is created or associated with  a different resource pool.  <p>  Returns null if the virtual machine is a template or the session has no access  to the resource pool. |
| <a href='parentVApp'>parentVApp</a> | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | true | None | Reference to the parent vApp. |
| <a href='resourceConfig'>resourceConfig</a> | [vim.ResourceConfigSpec](vim.ResourceConfigSpec.md "vim.ResourceConfigSpec") | true | None | The resource configuration for a virtual machine. The shares  in this specification are evaluated relative to the resource pool  to which it is assigned. This will return null if the product  the virtual machine is registered on does not support resource  configuration.  <p>  To retrieve the configuration, you typically use  <a href="vim.ResourcePool.md#childConfiguration">childConfiguration</a>.  <p>  To change the configuration, use  <a href="vim.ResourcePool.md#updateChildResourceConfiguration">UpdateChildResourceConfiguration</a>. |
| <a href='runtime'>runtime</a> | [vim.vm.RuntimeInfo](vim.vm.RuntimeInfo.md "vim.vm.RuntimeInfo") | None | None | Execution state and history for this virtual machine.  <p>  The contents of this property change when:  <ul>  <li>the virtual machine's power state changes.</li>  <li>an execution message is pending.</li>  <li>an event occurs.</li>  </ul> |
| <a href='guest'>guest</a> | [vim.vm.GuestInfo](vim.vm.GuestInfo.md "vim.vm.GuestInfo") | true | None | Information about VMware Tools and about the virtual machine  from the perspective of VMware Tools.  Information about the guest operating system is available in VirtualCenter. Guest  operating system information reflects the last known state of the virtual machine.  For powered on machines, this is current information. For powered off machines,  this is the last recorded state before the virtual machine was powered off. |
| <a href='summary'>summary</a> | [vim.vm.Summary](vim.vm.Summary.md "vim.vm.Summary") | None | None | Basic information about this virtual machine. This includes:  <ul>  <li>runtimeInfo</li>  <li>guest</li>  <li>basic configuration</li>  <li>alarms</li>  <li>performance information</li>  </ul> |
| <a href='datastore'>datastore</a> | [vim.Datastore](vim.Datastore.md "vim.Datastore") | true | System.View | A collection of references to the subset of datastore objects in the datacenter   that is used by this virtual machine. |
| <a href='network'>network</a> | [vim.Network](vim.Network.md "vim.Network") | true | System.View | A collection of references to the subset of network objects in the datacenter that   is used by this virtual machine. |
| <a href='snapshot'>snapshot</a> | [vim.vm.SnapshotInfo](vim.vm.SnapshotInfo.md "vim.vm.SnapshotInfo") | true | None | Current snapshot and tree.  The property is valid if snapshots have been created  for this virtual machine.  <p>  The contents of this property change in response to the methods:  <ul>  <li><a href="vim.VirtualMachine.md#createSnapshot">CreateSnapshot_Task</a></li>  <li><a href="vim.VirtualMachine.md#revertToCurrentSnapshot">RevertToCurrentSnapshot_Task</a></li>  <li><a href="vim.vm.Snapshot.md#remove">RemoveSnapshot_Task</a></li>  <li><a href="vim.vm.Snapshot.md#revert">RevertToSnapshot_Task</a></li>  <li><a href="vim.VirtualMachine.md#removeAllSnapshots">RemoveAllSnapshots_Task</a></li>  </ul> |
| <a href='rootSnapshot'>rootSnapshot</a> | [vim.vm.Snapshot](vim.vm.Snapshot.md "vim.vm.Snapshot") | true | None | The roots of all snapshot trees for the virtual machine. |
| <a href='guestHeartbeatStatus'>guestHeartbeatStatus</a> | [vim.ManagedEntity.Status](vim.ManagedEntity.Status.md "vim.ManagedEntity.Status") | None | None | The guest heartbeat.  The heartbeat status is classified as:   <ul>   <li> gray - VMware Tools are not installed or not running.</li>   <li> red - No heartbeat. Guest operating system may have stopped responding.</li>   <li> yellow - Intermittent heartbeat. May be due to guest load.</li>   <li> green - Guest operating system is responding normally.</li>   </ul>   The guest heartbeat is a statistics metric. Alarms can be configured on   this metric to trigger emails or other actions. |


RefreshStorageInfo()
--------------------

| service name | RefreshStorageInfo |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




CreateSnapshot([name](#string "string"), [description](#string "string"))
-------------------------------------------------------------------------
 raises [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.SnapshotFault](vim.fault.SnapshotFault.md "vim.fault.SnapshotFault")

---
| service name | CreateSnapshot |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.State.CreateSnapshot |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.SnapshotFault](vim.fault.SnapshotFault.md "vim.fault.SnapshotFault") | if an error occurs during the snapshot operation.          Typically a more specific fault like MultipleSnapshotsNotSupported          is thrown. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if the virtual machine's configuration is invalid.          Typically, a more specific fault like InvalidSnapshotState is thrown. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a problem with creating or accessing one          or more files needed for this operation. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the specified snapshot name is invalid. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the          virtual machine's current state. For example, the virtual machine          configuration information is not available. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host product does not support snapshots or if the host  does not support quiesced snapshots and the quiesce parameter is set to true; or  if the virtual machine is a Fault Tolerance primary or secondary |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the operation cannot be performed in the current          power state of the virtual machine. |




RevertToCurrentSnapshot([host](vim.HostSystem.md "vim.HostSystem"))
-------------------------------------------------------------------
 raises [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.DisallowedOperationOnFailoverHost](vim.fault.DisallowedOperationOnFailoverHost.md "vim.fault.DisallowedOperationOnFailoverHost"), [vim.fault.SnapshotFault](vim.fault.SnapshotFault.md "vim.fault.SnapshotFault"), [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault")

---
| service name | RevertToCurrentSnapshot |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.State.RevertToSnapshot |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.SnapshotFault](vim.fault.SnapshotFault.md "vim.fault.SnapshotFault") | if an error occurs during the snapshot operation.           Typically, a more specific fault like InvalidSnapshotFormat           is thrown. |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | if this operation would violate a resource           usage policy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the           virtual machine's current state. For example, if the virtual machine           configuration information is not available or if an OVF consumer is           blocking the operation. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if a configuration issue prevents the power-on. Typically, a           more specific fault, such as UnsupportedVmxLocation, is thrown. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the virtual machine does not have a current snapshot. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host product does not support snapshots. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the operation cannot be performed in the current           power state of the virtual machine. |
| [vim.fault.DisallowedOperationOnFailoverHost](vim.fault.DisallowedOperationOnFailoverHost.md "vim.fault.DisallowedOperationOnFailoverHost") | if the virtual machine is being           reverted to a powered on state and the host specified is a failover host.           See <a href="vim.cluster.FailoverHostAdmissionControlPolicy.md">ClusterFailoverHostAdmissionControlPolicy</a>. |




RemoveAllSnapshots()
--------------------
 raises [vim.fault.SnapshotFault](vim.fault.SnapshotFault.md "vim.fault.SnapshotFault"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | RemoveAllSnapshots |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.State.RemoveSnapshot |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the          virtual machine's current state. For example, if the virtual machine          configuration information is not available. |
| [vim.fault.SnapshotFault](vim.fault.SnapshotFault.md "vim.fault.SnapshotFault") | if an error occurs during the snapshot operation.          Typically, a more specific fault like InvalidSnapshotFormat          is thrown. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host product does not support snapshots. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the operation cannot be performed in the current          power state of the virtual machine. |




ConsolidateVMDisks()
--------------------
 raises [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | ConsolidateVMDisks |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#None) |
| privilege    | VirtualMachine.State.RemoveSnapshot |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the          virtual machine's current state. For example, if the virtual          machine configuration information is not available. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if if there is a problem creating or accessing the          virtual machine's files for this operation. Typically a more          specific fault for example <a href="vim.fault.NoDiskSpace.md">NoDiskSpace</a> is          thrown. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if a virtual machine configuration issue prevents          consolidation.  Typically, a more specific fault is thrown          such as <a href="vim.fault.InvalidDiskFormat.md">InvalidDiskFormat</a> if a disk cannot          be read, or <a href="vim.fault.InvalidSnapshotFormat.md">InvalidSnapshotFormat</a> if the          snapshot configuration is invalid. |




EstimateStorageForConsolidateSnapshots()
----------------------------------------
 raises [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | EstimateStorageForConsolidateSnapshots |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#None) |
| privilege    | VirtualMachine.State.RemoveSnapshot |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the          virtual machine's current state. For example, if the virtual machine          configuration information is not available. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if if there is a problem accessing the          virtual machine's files for this operation. Typically a more          specific fault <a href="vim.fault.FileLocked.md">FileLocked</a> is thrown. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if a virtual machine configuration issue prevents          the estimation.  Typically, a more specific fault is thrown. |




ReconfigVM([spec](vim.vm.ConfigSpec.md "vim.vm.ConfigSpec"))
------------------------------------------------------------
 raises [vim.fault.CpuHotPlugNotSupported](vim.fault.CpuHotPlugNotSupported.md "vim.fault.CpuHotPlugNotSupported"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess"), [vim.fault.VmWwnConflict](vim.fault.VmWwnConflict.md "vim.fault.VmWwnConflict"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.TooManyDevices](vim.fault.TooManyDevices.md "vim.fault.TooManyDevices"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault"), [vim.fault.MemoryHotPlugNotSupported](vim.fault.MemoryHotPlugNotSupported.md "vim.fault.MemoryHotPlugNotSupported")

---
| service name | ReconfigVM |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | dynamic |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if the spec is invalid. Typically, a more specific subclass          is thrown. |
| [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess") | if the changeVersion does not match the server's          changeVersion for the configuration. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a problem creating or accessing the virtual machine's          files for this operation. Typically a more specific fault like NoDiskSpace          or FileAlreadyExists is thrown. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the specified name is invalid. |
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if the specified name already exists in the parent folder. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed in the current state           of the virtual machine. For example, because the virtual machine's           configuration is not available. |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | if this operation would violate a resource          usage policy. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | vim.fault.InvalidDatastore |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the power state is poweredOn and the virtual hardware          cannot support the configuration changes. |
| [vim.fault.TooManyDevices](vim.fault.TooManyDevices.md "vim.fault.TooManyDevices") | if the device specifications exceed the allowed limits. |
| [vim.fault.CpuHotPlugNotSupported](vim.fault.CpuHotPlugNotSupported.md "vim.fault.CpuHotPlugNotSupported") | if the current configuration of the VM does not                                 support hot-plugging of CPUs. |
| [vim.fault.MemoryHotPlugNotSupported](vim.fault.MemoryHotPlugNotSupported.md "vim.fault.MemoryHotPlugNotSupported") | if the current configuration of the VM does not                                    support hot-plugging of memory. |
| [vim.fault.VmWwnConflict](vim.fault.VmWwnConflict.md "vim.fault.VmWwnConflict") | if the WWN of the virtual machine has been used by           other virtual machines. |




UpgradeVM([version](#string "string"))
--------------------------------------
 raises [vim.fault.AlreadyUpgraded](vim.fault.AlreadyUpgraded.md "vim.fault.AlreadyUpgraded"), [vim.fault.NoDiskFound](vim.fault.NoDiskFound.md "vim.fault.NoDiskFound"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | UpgradeVM |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Config.UpgradeVirtualHardware |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the host is in maintenance mode,                       if an invalid version string is specified, or                       if the virtual machine is in a state in which the operation                       cannot be performed. For example, if the configuration                       information is not available. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.AlreadyUpgraded](vim.fault.AlreadyUpgraded.md "vim.fault.AlreadyUpgraded") | if the virtual machine's hardware is already up-to-date. |
| [vim.fault.NoDiskFound](vim.fault.NoDiskFound.md "vim.fault.NoDiskFound") | if no virtual disks are attached to this virtual machine. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the power state is not poweredOff. |




ExtractOvfEnvironment()
-----------------------
 raises [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | ExtractOvfEnvironment |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | VApp.ExtractOvfEnvironment |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the virtual machine is not running |




PowerOnVM([host](vim.HostSystem.md "vim.HostSystem"))
-----------------------------------------------------
 raises [vmodl.fault.NotEnoughLicenses](vmodl.fault.NotEnoughLicenses.md "vmodl.fault.NotEnoughLicenses"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.DisallowedOperationOnFailoverHost](vim.fault.DisallowedOperationOnFailoverHost.md "vim.fault.DisallowedOperationOnFailoverHost"), [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault")

---
| service name | PowerOnVM |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.PowerOn |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the host is in maintenance mode or if          the virtual machine's configuration information is not available. |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | if this operation would violate a resource          usage policy. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if a configuration issue prevents the power-on.          Typically, a more specific fault, such as UnsupportedVmxLocation, is          thrown. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a problem accessing the virtual machine on the          filesystem. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the power state is poweredOn. |
| [vmodl.fault.NotEnoughLicenses](vmodl.fault.NotEnoughLicenses.md "vmodl.fault.NotEnoughLicenses") | if there are not enough licenses to power on this                            virtual machine. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the virtual machine is marked as a template. |
| [vim.fault.DisallowedOperationOnFailoverHost](vim.fault.DisallowedOperationOnFailoverHost.md "vim.fault.DisallowedOperationOnFailoverHost") | if the host specified is a failover          host. See <a href="vim.cluster.FailoverHostAdmissionControlPolicy.md">ClusterFailoverHostAdmissionControlPolicy</a>. |




PowerOffVM()
------------
 raises [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | PowerOffVM |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.PowerOff |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the          virtual machine's current state. For example, if the virtual machine          configuration information is not available. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the power state is not poweredOn. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the virtual machine is marked as a template. |




SuspendVM()
-----------
 raises [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | SuspendVM |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.Suspend |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the          virtual machine's current state. For example, if the virtual machine          configuration information is not available. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the power state is not poweredOn. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the virtual machine is marked as a template. |




ResetVM()
---------
 raises [vmodl.fault.NotEnoughLicenses](vmodl.fault.NotEnoughLicenses.md "vmodl.fault.NotEnoughLicenses"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | ResetVM |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.Reset |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the host is in maintenance mode. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the power state is suspended. |
| [vmodl.fault.NotEnoughLicenses](vmodl.fault.NotEnoughLicenses.md "vmodl.fault.NotEnoughLicenses") | if there are not enough licenses to reset  this virtual machine. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the virtual machine is marked as a template. |




ShutdownGuest()
---------------
 raises [vim.fault.ToolsUnavailable](vim.fault.ToolsUnavailable.md "vim.fault.ToolsUnavailable"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | ShutdownGuest |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.PowerOff |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.ToolsUnavailable](vim.fault.ToolsUnavailable.md "vim.fault.ToolsUnavailable") | if VMware Tools is not running. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the          virtual machine's current state. For example, if the virtual machine          configuration information is not available. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the power state is not powered on. |




RebootGuest()
-------------
 raises [vim.fault.ToolsUnavailable](vim.fault.ToolsUnavailable.md "vim.fault.ToolsUnavailable"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | RebootGuest |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.Reset |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.ToolsUnavailable](vim.fault.ToolsUnavailable.md "vim.fault.ToolsUnavailable") | if VMware Tools is not running. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the          virtual machine's current state. For example, if the virtual machine          configuration information is not available. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the power state is not powered on. |




StandbyGuest()
--------------
 raises [vim.fault.ToolsUnavailable](vim.fault.ToolsUnavailable.md "vim.fault.ToolsUnavailable"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | StandbyGuest |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.Suspend |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.ToolsUnavailable](vim.fault.ToolsUnavailable.md "vim.fault.ToolsUnavailable") | if VMware Tools is not running. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the          virtual machine's current state. For example, if the virtual machine          configuration information is not available. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the power state is not powered on. |




AnswerVM([questionId](#string "string"), [answerChoice](#string "string"))
--------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess")

---
| service name | AnswerVM |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.AnswerQuestion |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess") | if the question has been or is being answered by          another thread or user. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the questionId does not apply to this virtual machine.     For example, this can happen if another client already answered the message. |




CustomizeVM([spec](vim.vm.customization.Specification.md "vim.vm.customization.Specification"))
-----------------------------------------------------------------------------------------------
 raises [vim.fault.CustomizationFault](vim.fault.CustomizationFault.md "vim.fault.CustomizationFault")

---
| service name | CustomizeVM |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Provisioning.Customize |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.CustomizationFault](vim.fault.CustomizationFault.md "vim.fault.CustomizationFault") | A subclass of CustomizationFault is thrown. |




CheckCustomizationSpec([spec](vim.vm.customization.Specification.md "vim.vm.customization.Specification"))
----------------------------------------------------------------------------------------------------------
 raises [vim.fault.CustomizationFault](vim.fault.CustomizationFault.md "vim.fault.CustomizationFault")

---
| service name | CheckCustomizationSpec |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Provisioning.Customize |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.CustomizationFault](vim.fault.CustomizationFault.md "vim.fault.CustomizationFault") | A subclass of CustomizationFault is thrown. |




MigrateVM([pool](vim.ResourcePool.md "vim.ResourcePool"), [host](vim.HostSystem.md "vim.HostSystem"), [priority](vim.VirtualMachine.MovePriority.md "vim.VirtualMachine.MovePriority"), [state](vim.VirtualMachine.PowerState.md "vim.VirtualMachine.PowerState"))
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.Timedout](vim.fault.Timedout.md "vim.fault.Timedout"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.MigrationFault](vim.fault.MigrationFault.md "vim.fault.MigrationFault"), [vim.fault.NoActiveHostInCluster](vim.fault.NoActiveHostInCluster.md "vim.fault.NoActiveHostInCluster"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault")

---
| service name | MigrateVM |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | dynamic |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.MigrationFault](vim.fault.MigrationFault.md "vim.fault.MigrationFault") | if it is not possible to migrate the virtual machine to          the destination host. This is typically due to hosts being incompatible,          such as mismatch in network polices or access to networks and datastores.          Typically, a more specific subclass is thrown. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if, in a case where the virtual machine          configuration file must be copied, the destination location for          that file does not have the necessary file access permissions. |
| [vim.fault.Timedout](vim.fault.Timedout.md "vim.fault.Timedout") | if one of the phases of the migration process times out. |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | if this operation would violate a resource          usage policy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the          virtual machine's current state or the target host's current state.          For example, if the virtual machine configuration information is not          available or if the target host is disconnected or in maintenance mode. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if the virtual machine is not compatible with the          destination host. Typically, a specific subclass of this exception is          thrown, such as IDEDiskNotSupported. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the virtual machine is marked as a template. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the target host and target pool are not          associated with the same compute resource or if the host parameter          is left unset when the target pool is associated with a non-DRS          cluster. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the state argument is set and the virtual          machine does not have that power state. |
| [vim.fault.NoActiveHostInCluster](vim.fault.NoActiveHostInCluster.md "vim.fault.NoActiveHostInCluster") | if a target host is not specified and the          cluster associated with the target pool does not contain at least one          potential target host. A host must be connected and not in maintenance          mode in order to be considered as a potential target host. |




RelocateVM([spec](vim.vm.RelocateSpec.md "vim.vm.RelocateSpec"), [priority](vim.VirtualMachine.MovePriority.md "vim.VirtualMachine.MovePriority"))
--------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.Timedout](vim.fault.Timedout.md "vim.fault.Timedout"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.MigrationFault](vim.fault.MigrationFault.md "vim.fault.MigrationFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.DisallowedOperationOnFailoverHost](vim.fault.DisallowedOperationOnFailoverHost.md "vim.fault.DisallowedOperationOnFailoverHost"), [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault")

---
| service name | RelocateVM |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Resource.ColdMigrate |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the          host or virtual machine's current state. For example, if the host is in          maintenance mode, or if the virtual machine's configuration information          is not available. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the          target datastores. |
| [vim.fault.MigrationFault](vim.fault.MigrationFault.md "vim.fault.MigrationFault") | if it is not possible to migrate the virtual machine to          the destination host. This is typically due to hosts being incompatible,          such as mismatch in network polices or access to networks and datastores.          Typically, a more specific subclass is thrown. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if the virtual machine is not compatible with the          destination host. Typically, a specific subclass of this exception is          thrown, such as IDEDiskNotSupported. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is an error accessing the virtual machine files. |
| [vim.fault.Timedout](vim.fault.Timedout.md "vim.fault.Timedout") | if one of the phases of the relocate process times out. |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | if this operation would violate a resource          usage policy. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the virtual machine is marked as a template. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | in the following cases:  <ul>     <li>  the target host and target pool are not associated with the           same compute resource</li>     <li>  the target pool represents a cluster without DRS enabled,           and the host is not specified</li>     <li>  Datastore in a diskLocator entry is not specified</li>     <li>  the specified device ID cannot be found in the virtual machine's current           configuration  </li>     <li>  the object specified in relocate cannot be found</li>  </ul> |
| [vim.fault.DisallowedOperationOnFailoverHost](vim.fault.DisallowedOperationOnFailoverHost.md "vim.fault.DisallowedOperationOnFailoverHost") | if the virtual machine is powered on          and is being migrated to a failover host. See          <a href="vim.cluster.FailoverHostAdmissionControlPolicy.md">ClusterFailoverHostAdmissionControlPolicy</a>. |




CloneVM([folder](vim.Folder.md "vim.Folder"), [name](#string "string"), [spec](vim.vm.CloneSpec.md "vim.vm.CloneSpec"))
-----------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.CustomizationFault](vim.fault.CustomizationFault.md "vim.fault.CustomizationFault"), [vim.fault.MigrationFault](vim.fault.MigrationFault.md "vim.fault.MigrationFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault")

---
| service name | CloneVM |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | None |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.CustomizationFault](vim.fault.CustomizationFault.md "vim.fault.CustomizationFault") | if a customization error happens.          Typically, a specific subclass of this exception is thrown. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the          virtual machine's current state. For example, if the virtual machine          configuration information is not available. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the          target datastores. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if the virtual machine is not compatible with the          destination host. Typically, a specific subclass of this exception is          thrown, such as IDEDiskNotSupported. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is an error accessing the virtual machine files. |
| [vim.fault.MigrationFault](vim.fault.MigrationFault.md "vim.fault.MigrationFault") | if it is not possible to migrate the virtual machine to          the destination host. This is typically due to hosts being incompatible,          such as mismatch in network polices or access to networks and datastores.          Typically, a more specific subclass is thrown. |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | if this operation would violate a resource          usage policy. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the host cannot run this virtual machine. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the operation is not supported by the current agent. |




ExportVm()
----------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | ExportVm |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | VApp.Export |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the virtual machine is powered on. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the          virtual machine's current state. For example, if the virtual machine          configuration information is not available. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is an error accessing the virtual machine files. |




MarkAsTemplate()
----------------
 raises [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | MarkAsTemplate |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Provisioning.MarkAsTemplate |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the          virtual machine's current state. For example, if the virtual machine          configuration information is not available. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if the template is incompatible with the host, such                         as the files are not accessible. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is an error accessing the virtual machine files. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if marking a virtual machine as a template is not supported. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the virtual machine is not powered off. |




MarkAsVirtualMachine([pool](vim.ResourcePool.md "vim.ResourcePool"), [host](vim.HostSystem.md "vim.HostSystem"))
----------------------------------------------------------------------------------------------------------------
 raises [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | MarkAsVirtualMachine |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Provisioning.MarkAsVM |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the virtual machine is not marked as a template. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the           target datastores. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if the virtual machine is not compatible with the           host. For example, a DisksNotSupported fault if the destination host           does not support the disk backings of the template. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is an error accessing the virtual machine files. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if marking a template as a virtual machine is not                         supported. |




UnregisterVM()
--------------
 raises [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | UnregisterVM |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Inventory.Unregister |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the virtual machine is powered on. |




ResetGuestInformation()
-----------------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | ResetGuestInformation |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Config.ResetGuestInfo |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the virtual machine is not powered off. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the virtual machine is marked as a template. |




MountToolsInstaller()
---------------------
 raises [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vim.fault.VmToolsUpgradeFault](vim.fault.VmToolsUpgradeFault.md "vim.fault.VmToolsUpgradeFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | MountToolsInstaller |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.ToolsInstall |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the virtual machine is not running,   or the VMware Tools CD is already mounted. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | vim.fault.VmConfigFault |
| [vim.fault.VmToolsUpgradeFault](vim.fault.VmToolsUpgradeFault.md "vim.fault.VmToolsUpgradeFault") | if the VMware Tools CD failed to mount. |




UnmountToolsInstaller()
-----------------------
 raises [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | UnmountToolsInstaller |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.ToolsInstall |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the virtual machine is not running,   VMware Tools is not running or the VMware Tools CD is already mounted. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | vim.fault.VmConfigFault |




UpgradeTools([installerOptions](#string "string"))
--------------------------------------------------
 raises [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.ToolsUnavailable](vim.fault.ToolsUnavailable.md "vim.fault.ToolsUnavailable"), [vim.fault.VmToolsUpgradeFault](vim.fault.VmToolsUpgradeFault.md "vim.fault.VmToolsUpgradeFault")

---
| service name | UpgradeTools |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.ToolsInstall |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the virtual machine is not running   or is suspended. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if an upgrade is already taking place. |
| [vim.fault.VmToolsUpgradeFault](vim.fault.VmToolsUpgradeFault.md "vim.fault.VmToolsUpgradeFault") | if the upgrade failed. |
| [vim.fault.ToolsUnavailable](vim.fault.ToolsUnavailable.md "vim.fault.ToolsUnavailable") | if VMware Tools is not running. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | vim.fault.VmConfigFault |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if upgrading tools is not supported. |




AcquireMksTicket()
------------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
### Deprecated
As of vSphere API 4.1, use <a href="vim.VirtualMachine.md#acquireTicket">AcquireTicket</a> instead.

| service name | AcquireMksTicket |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.ConsoleInteract |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if it cannot retrieve TCP binding           information about the client connection. For example,           TCP binding information is not available for a client           connection that is not TCP-based. |




AcquireTicket([ticketType](#string "string"))
---------------------------------------------
 raises [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | AcquireTicket |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#None) |
| privilege    | dynamic |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the virtual machine is not connected. |




SetScreenResolution()
---------------------
 raises [vim.fault.ToolsUnavailable](vim.fault.ToolsUnavailable.md "vim.fault.ToolsUnavailable"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | SetScreenResolution |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.ConsoleInteract |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the virtual machine is not connected. |
| [vim.fault.ToolsUnavailable](vim.fault.ToolsUnavailable.md "vim.fault.ToolsUnavailable") | if VMware Tools is not running. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the Guest Operating system does          not support setting the screen resolution. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the power state is not poweredOn. |




DefragmentAllDisks()
--------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | DefragmentAllDisks |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.DefragmentAllDisks |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the virtual machine is not connected. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the virtual machine is poweredOn. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is an error accessing the disk files. |




CreateSecondaryVM([host](vim.HostSystem.md "vim.HostSystem"))
-------------------------------------------------------------
 raises [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.VmFaultToleranceIssue](vim.fault.VmFaultToleranceIssue.md "vim.fault.VmFaultToleranceIssue")

---
| service name | CreateSecondaryVM |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.CreateSecondary |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the virtual machine's configuration information          is not available. |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | if this operation would violate a resource          usage policy. |
| [vim.fault.VmFaultToleranceIssue](vim.fault.VmFaultToleranceIssue.md "vim.fault.VmFaultToleranceIssue") | if any error is encountered with the          fault tolerance configuration of the virtual machine. Typically,          a more specific fault like FaultToleranceNotLicensed is thrown. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a problem accessing the virtual machine on the          filesystem. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if a configuration issue prevents creating the secondary.          Typically, a more specific fault such as          VmConfigIncompatibleForFaultTolerance is thrown. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the virtual machine is marked as a template, or          it is not in a vSphere HA enabled cluster. |
| [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound") | if a host is specified and it does not exist. |




TurnOffFaultToleranceForVM()
----------------------------
 raises [vim.fault.VmFaultToleranceIssue](vim.fault.VmFaultToleranceIssue.md "vim.fault.VmFaultToleranceIssue"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | TurnOffFaultToleranceForVM |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.TurnOffFaultTolerance |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.VmFaultToleranceIssue](vim.fault.VmFaultToleranceIssue.md "vim.fault.VmFaultToleranceIssue") | if any error is encountered with the          fault tolerance configuration of the virtual machine. Typically,          a more specific fault like InvalidOperationOnSecondaryVm is thrown. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the host is in maintenance mode or if          the virtual machine's configuration information is not available. |




MakePrimaryVM([vm](vim.VirtualMachine.md "vim.VirtualMachine"))
---------------------------------------------------------------
 raises [vim.fault.VmFaultToleranceIssue](vim.fault.VmFaultToleranceIssue.md "vim.fault.VmFaultToleranceIssue"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | MakePrimaryVM |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.MakePrimary |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.VmFaultToleranceIssue](vim.fault.VmFaultToleranceIssue.md "vim.fault.VmFaultToleranceIssue") | if any error is encountered with the          fault tolerance configuration of the virtual machine. Typically,          a more specific fault like InvalidOperationOnSecondaryVm is thrown. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the host is in maintenance mode or if          the virtual machine's configuration information is not available. |




TerminateFaultTolerantVM([vm](vim.VirtualMachine.md "vim.VirtualMachine"))
--------------------------------------------------------------------------
 raises [vim.fault.VmFaultToleranceIssue](vim.fault.VmFaultToleranceIssue.md "vim.fault.VmFaultToleranceIssue"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | TerminateFaultTolerantVM |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.TerminateFaultTolerantVM |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.VmFaultToleranceIssue](vim.fault.VmFaultToleranceIssue.md "vim.fault.VmFaultToleranceIssue") | if any error is encountered with the          fault tolerance configuration of the virtual machine. Typically,          a more specific fault like InvalidOperationOnSecondaryVm is thrown. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the host is in maintenance mode or if          the virtual machine's configuration information is not available. |




DisableSecondaryVM([vm](vim.VirtualMachine.md "vim.VirtualMachine"))
--------------------------------------------------------------------
 raises [vim.fault.VmFaultToleranceIssue](vim.fault.VmFaultToleranceIssue.md "vim.fault.VmFaultToleranceIssue"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | DisableSecondaryVM |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.DisableSecondary |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.VmFaultToleranceIssue](vim.fault.VmFaultToleranceIssue.md "vim.fault.VmFaultToleranceIssue") | if any error is encountered with the          fault tolerance configuration of the virtual machine. Typically,          a more specific fault like InvalidOperationOnSecondaryVm is thrown. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the host is in maintenance mode or if          the virtual machine's configuration information is not available. |




EnableSecondaryVM([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [host](vim.HostSystem.md "vim.HostSystem"))
---------------------------------------------------------------------------------------------------------------
 raises [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound"), [vim.fault.VmFaultToleranceIssue](vim.fault.VmFaultToleranceIssue.md "vim.fault.VmFaultToleranceIssue"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | EnableSecondaryVM |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.EnableSecondary |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.VmFaultToleranceIssue](vim.fault.VmFaultToleranceIssue.md "vim.fault.VmFaultToleranceIssue") | if any error is encountered with the          fault tolerance configuration of the virtual machine. Typically,          a more specific fault like InvalidOperationOnSecondaryVm is thrown. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the virtual machine's configuration information is not          available, if the secondary virtual machine is not disabled, or if a          power-on is attempted and one is already in progress. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if a configuration issue prevents enabling the secondary.          Typically, a more specific fault such as          VmConfigIncompatibleForFaultTolerance is thrown. |
| [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound") | if a host is specified and it does not exist. |




SetDisplayTopology([displays](vim.VirtualMachine.DisplayTopology.md "vim.VirtualMachine.DisplayTopology"))
----------------------------------------------------------------------------------------------------------
 raises [vim.fault.ToolsUnavailable](vim.fault.ToolsUnavailable.md "vim.fault.ToolsUnavailable"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | SetDisplayTopology |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.ConsoleInteract |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the virtual machine is not connected. |
| [vim.fault.ToolsUnavailable](vim.fault.ToolsUnavailable.md "vim.fault.ToolsUnavailable") | if VMware Tools is not running. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the Guest Operating system does          not support setting the display topology |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the power state is not poweredOn. |




StartRecording([name](#string "string"), [description](#string "string"))
-------------------------------------------------------------------------
 raises [vim.fault.VmConfigIncompatibleForRecordReplay](vim.fault.VmConfigIncompatibleForRecordReplay.md "vim.fault.VmConfigIncompatibleForRecordReplay"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vim.fault.HostIncompatibleForRecordReplay](vim.fault.HostIncompatibleForRecordReplay.md "vim.fault.HostIncompatibleForRecordReplay"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.SnapshotFault](vim.fault.SnapshotFault.md "vim.fault.SnapshotFault"), [vim.fault.RecordReplayDisabled](vim.fault.RecordReplayDisabled.md "vim.fault.RecordReplayDisabled")

---
### Deprecated
As of vsphere API 5.1

| service name | StartRecording |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.Record |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the          virtual machine's current state. For example, the virtual machine          configuration information is not available. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the operation cannot be performed in the          current power state of the virtual machine. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a problem with creating or accessing one          or more files needed for this operation. |
| [vim.fault.SnapshotFault](vim.fault.SnapshotFault.md "vim.fault.SnapshotFault") | if an error occurs during the snapshot operation.          Typically, a more specific fault like MultipleSnapshotsNotSupported          is thrown. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | vim.fault.VmConfigFault |
| [vim.fault.RecordReplayDisabled](vim.fault.RecordReplayDisabled.md "vim.fault.RecordReplayDisabled") | if the record/replay config flag has not been          enabled for this virtual machine. |
| [vim.fault.HostIncompatibleForRecordReplay](vim.fault.HostIncompatibleForRecordReplay.md "vim.fault.HostIncompatibleForRecordReplay") | if the virtual machine is located          on a host that does not support record/replay. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the specified snapshot name is invalid. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host product does not support record          functionality or if the virtual machine does not support this |
| [vim.fault.VmConfigIncompatibleForRecordReplay](vim.fault.VmConfigIncompatibleForRecordReplay.md "vim.fault.VmConfigIncompatibleForRecordReplay") | if the virtual machine          configuration is incompatible for recording. |




StopRecording()
---------------
 raises [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.SnapshotFault](vim.fault.SnapshotFault.md "vim.fault.SnapshotFault")

---
### Deprecated
As of vsphere API 5.1

| service name | StopRecording |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.Record |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the          virtual machine's current state. For example, the virtual machine          does not have an active recording session. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the operation cannot be performed in the current          power state of the virtual machine. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a problem with creating or accessing one          or more files needed for this operation. |
| [vim.fault.SnapshotFault](vim.fault.SnapshotFault.md "vim.fault.SnapshotFault") | if an error occurs during the snapshot operation.          Typically, a more specific fault like InvalidSnapshotFormat          is thrown. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host product does not support record/replay          functionality or if the virtual machine does not support this          capability. |




StartReplaying([replaySnapshot](vim.vm.Snapshot.md "vim.vm.Snapshot"))
----------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vim.fault.HostIncompatibleForRecordReplay](vim.fault.HostIncompatibleForRecordReplay.md "vim.fault.HostIncompatibleForRecordReplay"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.VmConfigIncompatibleForRecordReplay](vim.fault.VmConfigIncompatibleForRecordReplay.md "vim.fault.VmConfigIncompatibleForRecordReplay"), [vim.fault.SnapshotFault](vim.fault.SnapshotFault.md "vim.fault.SnapshotFault"), [vim.fault.RecordReplayDisabled](vim.fault.RecordReplayDisabled.md "vim.fault.RecordReplayDisabled")

---
### Deprecated
As of vsphere API 5.1

| service name | StartReplaying |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.Replay |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the          virtual machine's current state. For example, the virtual machine          configuration information is not available. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the operation cannot be performed in the          current power state of the virtual machine. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a problem with creating or accessing one          or more files needed for this operation. |
| [vim.fault.SnapshotFault](vim.fault.SnapshotFault.md "vim.fault.SnapshotFault") | if an error occurs during the snapshot operation.          Typically, a more specific fault like InvalidSnapshotFormat          is thrown. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if replaySnapshot is no longer present. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | vim.fault.VmConfigFault |
| [vim.fault.RecordReplayDisabled](vim.fault.RecordReplayDisabled.md "vim.fault.RecordReplayDisabled") | if the record/replay config flag has not been          enabled for this virtual machine. |
| [vim.fault.HostIncompatibleForRecordReplay](vim.fault.HostIncompatibleForRecordReplay.md "vim.fault.HostIncompatibleForRecordReplay") | if the virtual machine is located          on a host that does not support record/replay. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host product does not support record/replay          functionality or if the virtual machine does not support this          capability. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if replaySnapshot is not a valid snapshot          associated with a recorded session on this virtual machine. |
| [vim.fault.VmConfigIncompatibleForRecordReplay](vim.fault.VmConfigIncompatibleForRecordReplay.md "vim.fault.VmConfigIncompatibleForRecordReplay") | if the virtual machine          configuration is incompatible for replaying. |




StopReplaying()
---------------
 raises [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.SnapshotFault](vim.fault.SnapshotFault.md "vim.fault.SnapshotFault")

---
### Deprecated
As of vsphere API 5.1

| service name | StopReplaying |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.Replay |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the          virtual machine's current state. For example, the virtual machine          does not have an active recording session. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the operation cannot be performed in the          current power state of the virtual machine. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a problem with creating or accessing one          or more files needed for this operation. |
| [vim.fault.SnapshotFault](vim.fault.SnapshotFault.md "vim.fault.SnapshotFault") | if an error occurs during the snapshot operation.          Typically, a more specific fault like InvalidSnapshotFormat          is thrown. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host product does not support record/replay          functionality or if the virtual machine does not support this          capability. |




PromoteDisks([disks](vim.vm.device.VirtualDisk.md "vim.vm.device.VirtualDisk"))
-------------------------------------------------------------------------------
 raises [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | PromoteDisks |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | VirtualMachine.Provisioning.PromoteDisks |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the virtual machine is not ready to respond to                       such requests. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the virtual machine is not powered off or suspended |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host doesnt support disk promotion APIs. |




CreateScreenshot()
------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | CreateScreenshot |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.CreateScreenshot |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a problem with creating or accessing one          or more files needed for this operation. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the virtual machine is not ready to respond to                       such requests. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the virtual machine is not powered on. |




QueryChangedDiskAreas([snapshot](vim.vm.Snapshot.md "vim.vm.Snapshot"), [changeId](#string "string"))
-----------------------------------------------------------------------------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | QueryChangedDiskAreas |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | VirtualMachine.Provisioning.DiskRandomRead |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if the virtual disk files cannot be accessed/queried. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the snapshot specified does not exist. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if deviceKey does not specify a virtual disk, startOffset          is beyond the end of the virtual disk or changeId is invalid or change          tracking is not supported for this particular disk. |




QueryUnownedFiles()
-------------------

| service name | QueryUnownedFiles |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | VirtualMachine.Config.QueryUnownedFiles |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|




reloadVirtualMachineFromPath([configurationPath](#string "string"))
-------------------------------------------------------------------
 raises [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | reloadVirtualMachineFromPath |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#None) |
| privilege    | VirtualMachine.Config.ReloadFromPath |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the virtual machine is powered on. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a problem creating or accessing the files           needed for this operation. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the virtual machine is busy or not ready to          respond to such requests. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if the format / configuration of the virtual machine           is invalid. Typically, a more specific fault is thrown such as           InvalidFormat if the configuration file cannot be read, or           InvalidDiskFormat if the disks cannot be read. |
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | if the virtual machine is already registered. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if invoked on ESX server or if invoked on a virtual           machine with the destination path for a template and vice-versa. |




QueryFaultToleranceCompatibility()
----------------------------------
 raises [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | QueryFaultToleranceCompatibility |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#None) |
| privilege    | VirtualMachine.Config.QueryFTCompatibility |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of          the virtual machine's current state. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if the virtual machine's configuration is invalid. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the virtual machine is a template or this operation          is not supported. |




TerminateVM()
-------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | TerminateVM |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#None) |
| privilege    | VirtualMachine.Interact.PowerOff |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the VM is not powered on or another issue prevents the          operation from being performed. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if this operation is not supported. |




