vim.event.TaskEvent
===================
inherits from [vim.event.Event](docs/vim.event.Event.md)


This event records the creation of a Task.   Note that the embedded TaskInfo object is a <i>snapshot</i> of the  Task state at the time of its creation, so its state will always be  "queued".  To find the current status of the task, query for the  current state of the Task using the eventChainId in the embedded  TaskInfo object.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| info | [vim.TaskInfo](vim.TaskInfo.md "vim.TaskInfo") | None | None | The information about the task. |


