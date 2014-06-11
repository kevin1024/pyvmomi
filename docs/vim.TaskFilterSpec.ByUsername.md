vim.TaskFilterSpec.ByUsername
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type enables you to filter task history according to    the users who performed the tasks.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| systemUser | bool | None | None | Whether or not to filter by system user.    If set to true, filters for system user event. |
| userList | string | true | None | Specifies the username list to use in the filter.    If not set, then all regular user tasks are collected. |


