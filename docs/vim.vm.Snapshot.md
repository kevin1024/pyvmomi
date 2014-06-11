vim.vm.Snapshot
===============
inherits from [vim.ExtensibleManagedObject](vim.ExtensibleManagedObject.md "vim.ExtensibleManagedObject")


The Snapshot managed object type specifies the interface to individual snapshots   of a virtual machine. Although these are managed objects, they are subordinate to    their virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='config'>config</a> | [vim.vm.ConfigInfo](vim.vm.ConfigInfo.md "vim.vm.ConfigInfo") | None | None | Information about the configuration of this virtual machine when this snapshot was    taken.   <p>   The datastore paths for the virtual machine disks point to the head of the disk    chain that represents the disk at this given snapshot. The fileInfo.fileLayout    field is not set.   <p> |
| <a href='childSnapshot'>childSnapshot</a> | [vim.vm.Snapshot](vim.vm.Snapshot.md "vim.vm.Snapshot") | true | None | All snapshots for which this snapshot is the parent. |


RevertToSnapshot([host](vim.HostSystem.md "vim.HostSystem"))
------------------------------------------------------------
 raises [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault")

---
| service name | RevertToSnapshot |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.State.RevertToSnapshot |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | if this operation would violate a resource           usage policy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed in the current state           of the virtual machine. For example, the virtual machine's configuration            is not available. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a problem accessing the virtual machine on the           filesystem. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if a configuration issue prevents the power-on. Typically, a            more specific fault, such as UnsupportedVmxLocation, is thrown. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host product does not support snapshots. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the operation cannot be performed in the current           power state of the virtual machine. |




RemoveSnapshot()
----------------
 raises [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | RemoveSnapshot |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.State.RemoveSnapshot |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |




RenameSnapshot([name](#string "string"), [description](#string "string"))
-------------------------------------------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | RenameSnapshot |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.State.RenameSnapshot |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the specified snapshot name is not valid. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed in the current state           of the virtual machine. For example, the virtual machine's configuration            is not available. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host product does not support snapshot rename. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the operation cannot be performed in the current           power state of the virtual machine. |




ExportSnapshot()
----------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | ExportSnapshot |
|:--|:--|
| since version | [vSphere API 5.5](vim.version.md#None) |
| privilege    | VApp.Export |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the          virtual machine's current state. For example, if the virtual machine          configuration information is not available. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is an error accessing the virtual machine files. |




