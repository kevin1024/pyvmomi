vim.event.EventFilterSpec.ByUsername
====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This option specifies users used to filter event history.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| systemUser | bool | None | None | filter by system user   true for system user event |
| userList | string | true | None | all interested username list   If this property is not set, then all regular user events are    collected |


