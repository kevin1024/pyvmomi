vim.host.FileAccess
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type contains a single access control   entry for a file permissions list.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| who | string | None | None | User or group to which the access applies. |
| what | string | None | None | Rights given to the user or group. |


