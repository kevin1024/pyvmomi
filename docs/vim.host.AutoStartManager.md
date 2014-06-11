vim.host.AutoStartManager
=========================


The AutoStartManager allows clients to invoke and set up the auto-start/auto-stop    order of virtual machines on a single host. Virtual machines configured to use    auto-start are automatically started or stopped when the host is started or shut    down. The AutoStartManager is available when clients connect directly to a host,    such as an ESX Server machine or through VirtualCenter.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='config'>config</a> | [vim.host.AutoStartManager.Config](vim.host.AutoStartManager.Config.md "vim.host.AutoStartManager.Config") | None | None |  |


ReconfigureAutostart([spec](vim.host.AutoStartManager.Config.md "vim.host.AutoStartManager.Config"))
----------------------------------------------------------------------------------------------------

| service name | ReconfigureAutostart |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.AutoStart |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




AutoStartPowerOn()
------------------

| service name | AutoStartPowerOn |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.AutoStart |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




AutoStartPowerOff()
-------------------

| service name | AutoStartPowerOff |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.AutoStart |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




