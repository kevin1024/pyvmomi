vim.TaskFilterSpec
==================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type defines the specification for the task filter used    to query tasks in the history collector database. The client creates a task    history collector with a filter specification, then retrieves the tasks from    the task history collector.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entity | [vim.TaskFilterSpec.ByEntity](vim.TaskFilterSpec.ByEntity.md "vim.TaskFilterSpec.ByEntity") | true | None | The filter specification for retrieving tasks by managed entity.   If not provided, then the tasks attached to all managed entities are    collected. |
| time | [vim.TaskFilterSpec.ByTime](vim.TaskFilterSpec.ByTime.md "vim.TaskFilterSpec.ByTime") | true | None | The filter specification for retrieving tasks by time.   If not provided, then the tasks with any time stamp are collected. |
| userName | [vim.TaskFilterSpec.ByUsername](vim.TaskFilterSpec.ByUsername.md "vim.TaskFilterSpec.ByUsername") | true | None | The filter specification for retrieving tasks by user name.   If not provided, then the tasks belonging to any user are collected. |
| state | [vim.TaskInfo.State](vim.TaskInfo.State.md "vim.TaskInfo.State") | true | None | This property, if provided, limits the set of collected tasks by their states.   Task states are enumerated in <a href="vim.TaskInfo.md#state">State</a>.   If not provided, tasks are collected regardless of their state. |
| alarm | [vim.alarm.Alarm](vim.alarm.Alarm.md "vim.alarm.Alarm") | true | None | This property, if provided, limits the set of collected tasks to those   associated with the specified alarm.   If not provided, tasks are collected regardless of their association with alarms. |
| scheduledTask | [vim.scheduler.ScheduledTask](vim.scheduler.ScheduledTask.md "vim.scheduler.ScheduledTask") | true | None | This property, if provided, limits the set of collected tasks to those   associated with the specified scheduled task.   If not provided, tasks are collected regardless of their association with any   scheduled task. |
| eventChainId | int | true | None | The filter specification for retrieving tasks by chain ID. If it is set,   tasks not with the given <a href="vim.TaskInfo.md#eventChainId">eventChainId</a> will be   filtered out. If the property is not set, tasks' chain ID is disregarded   for filtering purposes. |
| tag | string | true | None | The filter specification for retrieving tasks by    <a href="vim.TaskInfo.md#changeTag">tag</a>. If it is set, tasks not with the given tag(s)   will be filtered out. If the property is not set, tasks' tag is disregarded for    filtering purposes. If it is set, and includes an empty string, tasks without a    tag will be returned. |
| parentTaskKey | string | true | None | The filter specification for retrieving tasks by   <a href="vim.TaskInfo.md#parentTaskKey">parentTaskKey</a>. If it is set, tasks not with the   given parentTaskKey(s) will be filtered out. If the property is not set,   tasks' parentTaskKey is disregarded for filtering purposes. |
| rootTaskKey | string | true | None | The filter specification for retrieving tasks by   <a href="vim.TaskInfo.md#rootTaskKey">rootTaskKey</a>. If it is set, tasks not with the   given rootTaskKey(s) will be filtered out. If the property is not set,   tasks' rootTaskKey is disregarded for filtering purposes. |


