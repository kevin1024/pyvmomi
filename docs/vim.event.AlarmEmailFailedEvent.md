vim.event.AlarmEmailFailedEvent
===============================
inherits from [vim.event.AlarmEvent](docs/vim.event.AlarmEvent.md)


This event records a failure to complete an alarm email notification.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entity | [vim.event.ManagedEntityEventArgument](vim.event.ManagedEntityEventArgument.md "vim.event.ManagedEntityEventArgument") | None | None | The entity with which the alarm is registered. |
| to | string | None | None | The destination email address. |
| reason | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | None | None | The reason for the failure. |


