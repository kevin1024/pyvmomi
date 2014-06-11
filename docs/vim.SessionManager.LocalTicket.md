vim.SessionManager.LocalTicket
==============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type contains the user name   and location of the file containing the password that   clients can use for one-time logon to a server.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| userName | string | None | None | User name to be used for logon. |
| passwordFilePath | string | None | None | Absolute local path to the file containing a one-time password. |


