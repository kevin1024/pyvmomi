vim.host.LocalAccountManager.PosixAccountSpecification
======================================================
inherits from [vim.host.LocalAccountManager.AccountSpecification](docs/vim.host.LocalAccountManager.AccountSpecification.md)


This data object type contains a POSIX-specific parameter   for local account creation.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| posixId | int | true | None | The user ID or group ID of a specified account.   <p/> |
| shellAccess | bool | true | None | Grants shell access if true. By default, shell access is disallowed.   <p/>   As of vSphere API 4.1, this property has effect only on users with Administrator   role on one or more VIM objects. For all others the default is applied.   <p/> |


