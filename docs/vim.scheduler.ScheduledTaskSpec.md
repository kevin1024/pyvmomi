vim.scheduler.ScheduledTaskSpec
===============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Parameters for scheduled task creation.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | Name of the scheduled task. |
| description | string | None | None | Description of the scheduled task. |
| enabled | bool | None | None | Flag to indicate whether the scheduled task is enabled or disabled. |
| scheduler | [vim.scheduler.TaskScheduler](vim.scheduler.TaskScheduler.md "vim.scheduler.TaskScheduler") | None | None | The time scheduler that determines when the scheduled task runs. |
| action | [vim.action.Action](vim.action.Action.md "vim.action.Action") | None | None | The action of the scheduled task, to be done when the scheduled task runs. |
| notification | string | true | None | The email notification.   If not set, this property is set to empty string, indicating no notification. |


