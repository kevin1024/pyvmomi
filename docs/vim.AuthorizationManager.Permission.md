vim.AuthorizationManager.Permission
===================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type provides assignment of some role access to    a principal on a specific entity.  A ManagedEntity is limited to    one permission per principal.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entity | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | true | None | Managed entity the permission is defined on.  Left unset   when calling setPermissions or resetPermissions, but present   for the results of permission queries. |
| principal | string | None | None | User or group receiving access in the form of   "login" for local or "DOMAIN\login" for users in a Windows domain. |
| group | bool | None | None | Whether principal refers to a user or a group.  True for   a group and false for a user. |
| roleId | int | None | None | Reference to the role providing the access. |
| propagate | bool | None | None | Whether or not this permission propagates down the hierarchy   to sub-entities. |


