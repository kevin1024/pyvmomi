vim.event.AlarmActionTriggeredEvent
===================================
inherits from [vim.event.AlarmEvent](docs/vim.event.AlarmEvent.md)


This event records that an alarm was triggered.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| source | [vim.event.ManagedEntityEventArgument](vim.event.ManagedEntityEventArgument.md "vim.event.ManagedEntityEventArgument") | None | None | The entity that triggered the alarm. |
| entity | [vim.event.ManagedEntityEventArgument](vim.event.ManagedEntityEventArgument.md "vim.event.ManagedEntityEventArgument") | None | None | The entity with which the alarm is registered. |


