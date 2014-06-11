vim.TaskFilterSpec.ByTime
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type specifies a time range used to filter task history.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| timeType | [vim.TaskFilterSpec.TimeOption](vim.TaskFilterSpec.TimeOption.md "vim.TaskFilterSpec.TimeOption") | None | None | The time stamp to filter: queued, started, or completed time. |
| beginTime | datetime | true | None | The beginning of the time range.   If this property is not specified, then tasks are collected from   the earliest time in the database.   <p>   When this property is specified, the time type field must also be specified. |
| endTime | datetime | true | None | The end of the time range.   If this property is not specified, then tasks are collected up to   the latest time in the database.   <p>   When this property is specified, the time type field must also be specified. |


