vim.scheduler.ScheduledTaskDescription
======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Static strings for scheduled tasks.  These strings are locale-specific.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| action | [vim.TypeDescription](vim.TypeDescription.md "vim.TypeDescription") | None | None | Action class descriptions for a scheduled task. |
| schedulerInfo | [vim.scheduler.ScheduledTaskDescription.SchedulerDetail](vim.scheduler.ScheduledTaskDescription.SchedulerDetail.md "vim.scheduler.ScheduledTaskDescription.SchedulerDetail") | None | None | Scheduler class description details. |
| state | [vim.ElementDescription](vim.ElementDescription.md "vim.ElementDescription") | None | None | <a href="vim.TaskInfo.State.md">TaskInfo State enum</a> |
| dayOfWeek | [vim.ElementDescription](vim.ElementDescription.md "vim.ElementDescription") | None | None | <a href="vim.scheduler.MonthlyByWeekdayTaskScheduler.DayOfWeek.md">MonthlyByWeekdayTaskScheduler Days of the week enum description</a> |
| weekOfMonth | [vim.ElementDescription](vim.ElementDescription.md "vim.ElementDescription") | None | None | <a href="vim.scheduler.MonthlyByWeekdayTaskScheduler.WeekOfMonth.md">MonthlyByWeekdayTaskScheduler Week of the month enum description</a> |


