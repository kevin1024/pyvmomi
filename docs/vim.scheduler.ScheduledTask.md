vim.scheduler.ScheduledTask
===========================
inherits from [vim.ExtensibleManagedObject](vim.ExtensibleManagedObject.md "vim.ExtensibleManagedObject")


The scheduled task object.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='info'>info</a> | [vim.scheduler.ScheduledTaskInfo](vim.scheduler.ScheduledTaskInfo.md "vim.scheduler.ScheduledTaskInfo") | None | None | Information about the current scheduled task. |


RemoveScheduledTask()
---------------------
 raises [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | RemoveScheduledTask |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | ScheduledTask.Delete |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the scheduled task is running. |




ReconfigureScheduledTask([spec](vim.scheduler.ScheduledTaskSpec.md "vim.scheduler.ScheduledTaskSpec"))
------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | ReconfigureScheduledTask |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | ScheduledTask.Edit |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the scheduled task is running. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the scheduled task name is empty or too long. |
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if a scheduled task with the name already exists. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the specification is invalid. |




RunScheduledTask()
------------------
 raises [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | RunScheduledTask |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | ScheduledTask.Run |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the scheduled task is running already. |




