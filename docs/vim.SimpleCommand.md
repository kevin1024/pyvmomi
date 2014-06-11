vim.SimpleCommand
=================
as of [VI API 2.5](vim.version.md#vim.version.version2)


A managed object that wraps the execution of a single arbitrary   command. The specific command executed is assumed to be known from   the service name by the client invoking this command.  This object   presents a generic interface for such services.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='encodingType'>encodingType</a> | [vim.SimpleCommand.Encoding](vim.SimpleCommand.Encoding.md "vim.SimpleCommand.Encoding") | None | None | The encoding type used in the result. |
| <a href='entity'>entity</a> | [vim.ServiceManager.ServiceInfo](vim.ServiceManager.ServiceInfo.md "vim.ServiceManager.ServiceInfo") | None | None | A description of the service. |


ExecuteSimpleCommand([arguments](#string "string"))
---------------------------------------------------

| service name | ExecuteSimpleCommand |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | Global.ServiceManagers |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|




