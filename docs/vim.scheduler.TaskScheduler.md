vim.scheduler.TaskScheduler
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The <a href="vim.scheduler.TaskScheduler.md">TaskScheduler</a> data object is the base type for the scheduler objects.   The hierarchy of scheduler objects is as follows:    <pre>     TaskScheduler         <a href="vim.scheduler.AfterStartupTaskScheduler.md">AfterStartupTaskScheduler</a>         <a href="vim.scheduler.OnceTaskScheduler.md">OnceTaskScheduler</a>         <a href="vim.scheduler.RecurrentTaskScheduler.md">RecurrentTaskScheduler</a>             <a href="vim.scheduler.HourlyTaskScheduler.md">HourlyTaskScheduler</a>                 <a href="vim.scheduler.DailyTaskScheduler.md">DailyTaskScheduler</a>                     <a href="vim.scheduler.WeeklyTaskScheduler.md">WeeklyTaskScheduler</a>                     <a href="vim.scheduler.MonthlyTaskScheduler.md">MonthlyTaskScheduler</a>                         <a href="vim.scheduler.MonthlyByDayTaskScheduler.md">MonthlyByDayTaskScheduler</a>                         <a href="vim.scheduler.MonthlyByWeekdayTaskScheduler.md">MonthlyByWeekdayTaskScheduler</a>   </pre>   <p>   Use a scheduler object to set the time(s) for task execution.    You can use two scheduling modes - single execution or   recurring execution:   <ul>      <li>Use the <a href="vim.scheduler.AfterStartupTaskScheduler.md">AfterStartupTaskScheduler</a> or the <a href="vim.scheduler.OnceTaskScheduler.md">OnceTaskScheduler</a>          to schedule a single instance of task execution.      <li>Use one of the recurrent task schedulers to schedule          hourly, daily, weekly, or monthly task execution.   </ul>   <p>   After you have established the task timing, use the scheduler   object for the <a href="vim.scheduler.ScheduledTaskSpec.md">ScheduledTaskSpec</a>   <a href="vim.scheduler.ScheduledTaskSpec.md#scheduler">scheduler</a> property value.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| activeTime | datetime | true | None | The time that the schedule for the task takes effect.   Task activation is distinct from task execution.   When you activate a task, its schedule starts,   and when the next execution time occurs, the task will run.   If you do not set activeTime, the activation time defaults to   the time that you create the scheduled task. |
| expireTime | datetime | true | None | The time the schedule for the task expires.   If you do not set expireTime, the schedule does not expire. |


