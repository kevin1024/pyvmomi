vim.event.EventDescription.EventArgDesc
=======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Describes an available event argument name for an Event type, which  can be used in <a href="vim.alarm.EventAlarmExpression.md">EventAlarmExpression</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | The name of the argument |
| type | string | None | None | The type of the argument. |
| description | [vim.ElementDescription](vim.ElementDescription.md "vim.ElementDescription") | true | None | The localized description of the event argument. The key holds  the localization prefix for the argument, which is decided by  the Event type that it is actually declared in, which may be a  base type of this event type. |


