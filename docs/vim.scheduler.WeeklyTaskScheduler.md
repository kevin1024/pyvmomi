vim.scheduler.WeeklyTaskScheduler
=================================
inherits from [vim.scheduler.DailyTaskScheduler](docs/vim.scheduler.DailyTaskScheduler.md)


The <a href="vim.scheduler.WeeklyTaskScheduler.md">WeeklyTaskScheduler</a> data object sets the time for weekly   task execution. You can set the schedule for task execution   on one or more days during the week, and you complete the schedule   by setting the inherited properties for the hour and minute.    <p>   By default the scheduler executes the task according to the    specified day(s) every week.    If you set the interval to a value greater than 1, the task will   execute at the specified weekly interval. (For example, an interval   of 2 will cause the task to execute on the specified days every 2 weeks.)

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| sunday | bool | None | None | The day or days of the week when the scheduled task will run.   At least one of the days must be true. |
| monday | bool | None | None |  |
| tuesday | bool | None | None |  |
| wednesday | bool | None | None |  |
| thursday | bool | None | None |  |
| friday | bool | None | None |  |
| saturday | bool | None | None |  |


