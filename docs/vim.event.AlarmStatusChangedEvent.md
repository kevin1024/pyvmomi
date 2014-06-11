vim.event.AlarmStatusChangedEvent
=================================
inherits from [vim.event.AlarmEvent](docs/vim.event.AlarmEvent.md)


This event records a status change for an alarm.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| source | [vim.event.ManagedEntityEventArgument](vim.event.ManagedEntityEventArgument.md "vim.event.ManagedEntityEventArgument") | None | None | The entity for which the alarm status has been changed. |
| entity | [vim.event.ManagedEntityEventArgument](vim.event.ManagedEntityEventArgument.md "vim.event.ManagedEntityEventArgument") | None | None | The entity with which the alarm is registered. |
| from | string | None | None | The original alarm status. |
| to | string | None | None | The new alarm status. |


