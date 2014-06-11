vim.host.ImageConfigManager
===========================
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


This managed object is the interface for   configuration of the ESX software image, including   properties such as acceptance level.   It is currently designed to be host agent specific.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


HostImageConfigGetAcceptance()
------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | HostImageConfigGetAcceptance |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version7) |
| privilege    | System.Read |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if the host acceptance setting is invalid.<br>See <a href="vim.host.ImageConfigManager.AcceptanceLevel.md">HostImageAcceptanceLevel</a><br> |




HostImageConfigGetProfile()
---------------------------

| service name | HostImageConfigGetProfile |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version7) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




UpdateHostImageAcceptanceLevel([newAcceptanceLevel](#string "string"))
----------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | UpdateHostImageAcceptanceLevel |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version7) |
| privilege    | Host.Config.Image |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if the acceptance level is raised and there are                           VIB packages that are not permitted by the                           higher acceptance level.<br>See <a href="vim.host.ImageConfigManager.AcceptanceLevel.md">HostImageAcceptanceLevel</a><br> |




