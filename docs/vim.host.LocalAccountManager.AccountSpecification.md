vim.host.LocalAccountManager.AccountSpecification
=================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type contains common parameters   for local account creation. The password and description properties   are not supported for group accounts on POSIX hosts.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | string | None | None | The ID of the specified account. |
| password | string | true | None | The password for a user or group. |
| description | string | true | None | The description of the specified account. |


