vim.event.EventFilterSpec.ByTime
================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This option specifies a time range used to filter event history.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| beginTime | datetime | true | None | The beginning of the time range.   If this property is not set, then events are collected from   the earliest time in the database. |
| endTime | datetime | true | None | The end of the time range.   If this property is not specified, then events are collected up to   the latest time in the database. |


