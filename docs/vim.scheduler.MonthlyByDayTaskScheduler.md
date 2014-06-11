vim.scheduler.MonthlyByDayTaskScheduler
=======================================
inherits from [vim.scheduler.MonthlyTaskScheduler](docs/vim.scheduler.MonthlyTaskScheduler.md)


The <a href="vim.scheduler.MonthlyByDayTaskScheduler.md">MonthlyByDayTaskScheduler</a> data object sets the time for monthly   task execution. You can set the schedule for task execution   on one day during the month, and you complete the schedule by    setting the inherited properties for the hour and minute.    <p>   By default the scheduler executes the task on the specified day   every month. If you set the interval to a value greater than 1,    the task will execute at the specified monthly interval.    (For example, an interval of 2 will cause the task to execute   on the specified day, hour, and minute every 2 months.)

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| day | int | None | None | The day in every month to run the scheduled task.   Valid values are 1 to 31.   <p>   In any month where the value of "day" exceeds the total number of days   in the month, the scheduled task will run on the last day of the month. |


