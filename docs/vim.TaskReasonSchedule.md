vim.TaskReasonSchedule
======================
inherits from [vim.TaskReason](docs/vim.TaskReason.md)


Indicates that the task was queued by a scheduled task.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | The name of the scheduled task that queued this task. |
| scheduledTask | [vim.scheduler.ScheduledTask](vim.scheduler.ScheduledTask.md "vim.scheduler.ScheduledTask") | None | None | The scheduledTask object that queued this task. |


