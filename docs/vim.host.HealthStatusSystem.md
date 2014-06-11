vim.host.HealthStatusSystem
===========================
as of [VI API 2.5](vim.version.md#vim.version.version2)


This managed object manages the health state of the host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='runtime'>runtime</a> | [vim.host.HealthStatusSystem.Runtime](vim.host.HealthStatusSystem.Runtime.md "vim.host.HealthStatusSystem.Runtime") | None | None |  |


RefreshHealthStatusSystem()
---------------------------

| service name | RefreshHealthStatusSystem |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




ResetSystemHealthInfo()
-----------------------

| service name | ResetSystemHealthInfo |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | Host.Config.Settings |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




