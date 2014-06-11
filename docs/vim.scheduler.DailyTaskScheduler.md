vim.scheduler.DailyTaskScheduler
================================
inherits from [vim.scheduler.HourlyTaskScheduler](docs/vim.scheduler.HourlyTaskScheduler.md)


The <a href="vim.scheduler.DailyTaskScheduler.md">DailyTaskScheduler</a> data object sets the time for daily   task execution. You set the hour and the inherited minute   property to complete the schedule. By default, the scheduled task   will run once every day at the specified hour and minute.    <p>   If you set the interval to a value greater than 1, the task will   execute at the specified daily interval. (For example, an interval   of 2 will cause the task to execute at the specified hour and minute   every 2 days.)

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| hour | int | None | None | The hour at which the <a href="vim.scheduler.RecurrentTaskScheduler.md">RecurrentTaskScheduler</a> runs the task.   Use UTC (Coordinated Universal Time) values in the range   0 to 23, where 0 = 12:00 a.m. (UTC) and 12 = 12:00 p.m. (UTC).   <p>   For vCenter 2.x and prior releases, use the server's local time.   For example, use Eastern Standard Time (EST) or Pacific Daylight Time (PDT),    rather than UTC. |


