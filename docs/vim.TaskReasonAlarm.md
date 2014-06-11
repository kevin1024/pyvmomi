vim.TaskReasonAlarm
===================
inherits from [vim.TaskReason](docs/vim.TaskReason.md)


Indicates that the task was queued by an alarm.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| alarmName | string | None | None | The name of the alarm that queued the task, retained in the history   collector database. |
| alarm | [vim.alarm.Alarm](vim.alarm.Alarm.md "vim.alarm.Alarm") | None | None | The alarm object that queued the task. |
| entityName | string | None | None | The name of the managed entity on which the alarm is triggered,   retained in the history collector database. |
| entity | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | None | None | The managed entity object on which the alarm is triggered. |


