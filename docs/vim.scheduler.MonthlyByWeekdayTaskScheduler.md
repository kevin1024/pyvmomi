vim.scheduler.MonthlyByWeekdayTaskScheduler
===========================================
inherits from [vim.scheduler.MonthlyTaskScheduler](docs/vim.scheduler.MonthlyTaskScheduler.md)


The <a href="vim.scheduler.MonthlyByWeekdayTaskScheduler.md">MonthlyByWeekdayTaskScheduler</a> data object sets the time for  monthly task execution. You identify a single day for task execution  by specifying the week of the month and day of the week, and you   complete the schedule by setting the inherited properties for the   hour and minute.  <p>  By default, the scheduler executes the task on the specified day  every month. If you set the interval to a value greater than 1,  the task will execute at the specified monthly interval. (For example,  an interval of 2 will cause the task to execute on the specified  day, hour, and minute every 2 months.)

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| offset | [vim.scheduler.MonthlyByWeekdayTaskScheduler.WeekOfMonth](vim.scheduler.MonthlyByWeekdayTaskScheduler.WeekOfMonth.md "vim.scheduler.MonthlyByWeekdayTaskScheduler.WeekOfMonth") | None | None | The week in the month during which the scheduled task is to run. |
| weekday | [vim.scheduler.MonthlyByWeekdayTaskScheduler.DayOfWeek](vim.scheduler.MonthlyByWeekdayTaskScheduler.DayOfWeek.md "vim.scheduler.MonthlyByWeekdayTaskScheduler.DayOfWeek") | None | None | The day in the week when the scheduled task is to run. |


