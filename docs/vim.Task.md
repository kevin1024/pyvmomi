vim.Task
========
inherits from [vim.ExtensibleManagedObject](vim.ExtensibleManagedObject.md "vim.ExtensibleManagedObject")


A task is used to monitor and potentially cancel long   running operations.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='info'>info</a> | [vim.TaskInfo](vim.TaskInfo.md "vim.TaskInfo") | None | None | Detailed information about this task. |


CancelTask()
------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | CancelTask |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Global.CancelTask |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | If the task is already canceled or completed. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | If the task is not cancelable. |




UpdateProgress()
----------------
 raises [vim.fault.OutOfBounds](vim.fault.OutOfBounds.md "vim.fault.OutOfBounds"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | UpdateProgress |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | Task.Update |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | If task is not running |
| [vim.fault.OutOfBounds](vim.fault.OutOfBounds.md "vim.fault.OutOfBounds") | VirtualCenter 2.x servers throw   this fault if percentDone is less than 0 or greater than 100.  Newer   versions behave as described above, and never throw this fault. |




SetTaskState([state](vim.TaskInfo.State.md "vim.TaskInfo.State"), [result](#object "object"), [fault](vmodl.MethodFault.md "vmodl.MethodFault"))
------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | SetTaskState |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | Task.Update |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | If attempting to change states after     task is completed or in error, or attempting to set the     result or fault incorrectly |




SetTaskDescription([description](vmodl.LocalizableMessage.md "vmodl.LocalizableMessage"))
-----------------------------------------------------------------------------------------

| service name | SetTaskDescription |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Task.Update |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




