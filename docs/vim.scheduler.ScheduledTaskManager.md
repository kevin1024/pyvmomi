vim.scheduler.ScheduledTaskManager
==================================


Object manager for scheduled tasks.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='scheduledTask'>scheduledTask</a> | [vim.scheduler.ScheduledTask](vim.scheduler.ScheduledTask.md "vim.scheduler.ScheduledTask") | true | System.View | All available scheduled tasks. |
| <a href='description'>description</a> | [vim.scheduler.ScheduledTaskDescription](vim.scheduler.ScheduledTaskDescription.md "vim.scheduler.ScheduledTaskDescription") | None | System.View | Static descriptive strings used in scheduled tasks. |


CreateScheduledTask([entity](vim.ManagedEntity.md "vim.ManagedEntity"), [spec](vim.scheduler.ScheduledTaskSpec.md "vim.scheduler.ScheduledTaskSpec"))
-----------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | CreateScheduledTask |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the scheduled task name is empty or too long. |
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if a scheduled task with the name already exists. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the specification is invalid. |




RetrieveEntityScheduledTask([entity](vim.ManagedEntity.md "vim.ManagedEntity"))
-------------------------------------------------------------------------------

| service name | RetrieveEntityScheduledTask |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




CreateObjectScheduledTask([obj](#vim.ExtensibleManagedObject "vim.ExtensibleManagedObject"), [spec](vim.scheduler.ScheduledTaskSpec.md "vim.scheduler.ScheduledTaskSpec"))
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | CreateObjectScheduledTask |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the scheduled task name is empty or too long. |
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if a scheduled task with the name already exists. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the specification is invalid. |




RetrieveObjectScheduledTask([obj](#vim.ExtensibleManagedObject "vim.ExtensibleManagedObject"))
----------------------------------------------------------------------------------------------

| service name | RetrieveObjectScheduledTask |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




