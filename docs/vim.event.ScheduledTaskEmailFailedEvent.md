vim.event.ScheduledTaskEmailFailedEvent
=======================================
inherits from [vim.event.ScheduledTaskEvent](docs/vim.event.ScheduledTaskEvent.md)


This event records the failure of an attempt to send a notification via email   for a scheduled task.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| to | string | None | None | The destination email address. |
| reason | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | None | None | The reason for the failure. |


