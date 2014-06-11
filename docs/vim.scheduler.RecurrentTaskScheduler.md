vim.scheduler.RecurrentTaskScheduler
====================================
inherits from [vim.scheduler.TaskScheduler](docs/vim.scheduler.TaskScheduler.md)


The <a href="vim.scheduler.RecurrentTaskScheduler.md">RecurrentTaskScheduler</a> data object is the base type for   the hierarchy that includes hourly, daily, weekly, and monthly task schedulers.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| interval | int | None | None | How often to run the scheduled task. The value must be greater than    or equal to 1 and less than 1000. The default value is 1.   The interval acts as a multiplier for the unit of time associated   with a particular scheduler (hours, days, weeks, or months).    For example, setting the <a href="vim.scheduler.HourlyTaskScheduler.md">HourlyTaskScheduler</a> interval    to 4 causes the task to run every 4 hours. |


