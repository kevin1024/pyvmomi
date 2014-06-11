vim.scheduler.ScheduledTaskInfo
===============================
inherits from [vim.scheduler.ScheduledTaskSpec](docs/vim.scheduler.ScheduledTaskSpec.md)


The scheduled task details.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| scheduledTask | [vim.scheduler.ScheduledTask](vim.scheduler.ScheduledTask.md "vim.scheduler.ScheduledTask") | None | None | Scheduled task object. |
| entity | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | None | None | The entity on which related events will be logged.  If the task is scheduled on a ManagedEntity, this   field will also reflect the same ManagedEntity.  If task is scheduled on a ManagedObject, this field   will have information about the entity on which  the events will be logged on behalf of the ManagedObject.  ManagedObject itself will be denoted by <a href="vim.scheduler.ScheduledTaskInfo.md#taskObject">taskObject</a> |
| lastModifiedTime | datetime | None | None | The time the scheduled task is created or modified. |
| lastModifiedUser | string | None | None | Last user that modified the scheduled task. |
| nextRunTime | datetime | true | None | The next time the scheduled task will run. |
| prevRunTime | datetime | true | None | The last time the scheduled task ran. |
| state | [vim.TaskInfo.State](vim.TaskInfo.State.md "vim.TaskInfo.State") | None | None | Scheduled task state. |
| error | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | The fault code when the scheduled task state is "error". |
| result | object | true | None | The operation result when the scheduled task state is "success". |
| progress | int | true | None | The task progress when the scheduled task state is "running". |
| activeTask | [vim.Task](vim.Task.md "vim.Task") | true | None | The running task instance when the scheduled task state is "running". |
| taskObject | vim.ExtensibleManagedObject | None | None | The object on which the scheduled task is defined.  This field will have information about either the   ManagedEntity or the ManagedObject on which the scheduled  task is defined. |


