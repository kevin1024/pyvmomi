vim.scheduler.HourlyTaskScheduler
=================================
inherits from [vim.scheduler.RecurrentTaskScheduler](docs/vim.scheduler.RecurrentTaskScheduler.md)


The <a href="vim.scheduler.HourlyTaskScheduler.md">HourlyTaskScheduler</a> data object sets the time for hourly   task execution. By default, the scheduled task will run once every hour,   at the specified minute.    <p>   If you set the interval to a value greater than 1, the task will   execute at the specified hourly interval. (For example, an interval   of 2 will cause the task to execute at the specified minute every 2 hours.)

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| minute | int | None | None | The minute at which the <a href="vim.scheduler.RecurrentTaskScheduler.md">RecurrentTaskScheduler</a> runs   the task. Specify the minute value as a UTC (Coordinated Univeral Time)    value in the range 0 to 59.    <p>   For vCenter 2.x and prior releases, use the server's local time.   For example, use Australia Northern Territory (UTC +9:30) or Indian (UTC +5:30)   time values, rather than a UTC value. |


