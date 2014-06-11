vim.event.AlarmScriptFailedEvent
================================
inherits from [vim.event.AlarmEvent](docs/vim.event.AlarmEvent.md)


This event records a failure to complete an alarm-triggered script.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entity | [vim.event.ManagedEntityEventArgument](vim.event.ManagedEntityEventArgument.md "vim.event.ManagedEntityEventArgument") | None | None | The entity with which the alarm is registered. |
| script | string | None | None | The script triggered by the alarm. |
| reason | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | None | None | The reason for the failure. |


