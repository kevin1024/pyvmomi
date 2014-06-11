vim.event.AlarmScriptCompleteEvent
==================================
inherits from [vim.event.AlarmEvent](docs/vim.event.AlarmEvent.md)


This event records the completion of an alarm-triggered script.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entity | [vim.event.ManagedEntityEventArgument](vim.event.ManagedEntityEventArgument.md "vim.event.ManagedEntityEventArgument") | None | None | The entity with which the alarm is registered. |
| script | string | None | None | The script triggered by the alarm. |


