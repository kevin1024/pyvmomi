vim.scheduler.OnceTaskScheduler
===============================
inherits from [vim.scheduler.TaskScheduler](docs/vim.scheduler.TaskScheduler.md)


The <a href="vim.scheduler.OnceTaskScheduler.md">OnceTaskScheduler</a> data object establishes the time for running   a scheduled task only once.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| runAt | datetime | true | None | The time a task will run.   If you do not set the time, it executes immediately. |


