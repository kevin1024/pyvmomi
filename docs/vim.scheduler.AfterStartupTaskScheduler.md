vim.scheduler.AfterStartupTaskScheduler
=======================================
inherits from [vim.scheduler.TaskScheduler](docs/vim.scheduler.TaskScheduler.md)


The <a href="vim.scheduler.AfterStartupTaskScheduler.md">AfterStartupTaskScheduler</a> data object establishes the time   that a scheduled task will run after the vCenter server restarts.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| minute | int | None | None | The delay in minutes after vCenter server is restarted.   The value must be greater than or equal to 0. |


