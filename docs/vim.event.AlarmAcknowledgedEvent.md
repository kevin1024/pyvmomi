vim.event.AlarmAcknowledgedEvent
================================
inherits from [vim.event.AlarmEvent](docs/vim.event.AlarmEvent.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


This event records the acknowledgement of an Alarm

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| source | [vim.event.ManagedEntityEventArgument](vim.event.ManagedEntityEventArgument.md "vim.event.ManagedEntityEventArgument") | None | None | The entity that triggered the alarm. |
| entity | [vim.event.ManagedEntityEventArgument](vim.event.ManagedEntityEventArgument.md "vim.event.ManagedEntityEventArgument") | None | None | The entity with which the alarm is registered. |


