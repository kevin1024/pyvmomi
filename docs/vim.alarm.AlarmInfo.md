vim.alarm.AlarmInfo
===================
inherits from [vim.alarm.AlarmSpec](docs/vim.alarm.AlarmSpec.md)


Attributes of an alarm.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | The unique key. |
| alarm | [vim.alarm.Alarm](vim.alarm.Alarm.md "vim.alarm.Alarm") | None | None | The alarm object. |
| entity | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | None | None | The entity on which the alarm is registered. |
| lastModifiedTime | datetime | None | None | The time the alarm was created or modified. |
| lastModifiedUser | string | None | None | User name that modified the alarm most recently. |
| creationEventId | int | None | None | The event ID that records the alarm creation. |


