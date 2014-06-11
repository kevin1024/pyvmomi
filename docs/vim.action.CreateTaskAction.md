vim.action.CreateTaskAction
===========================
inherits from [vim.action.Action](docs/vim.action.Action.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This data object type specifies the type of task to be created   when this action is triggered.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| taskTypeId | string | None | None | Extension registered task type identifier   for type of task being created. |
| cancelable | bool | None | None | Whether the task should be cancelable. |


