vim.alarm.EventAlarmExpression.Comparison
=========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Encapsulates Comparison of an event's attribute to a value.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| attributeName | string | None | None | The attribute of the event to compare |
| operator | string | None | None | An operator from the list above |
| value | string | None | None | The value to compare against |


