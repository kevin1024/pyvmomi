vim.host.EsxAgentHostManager
============================
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


This managed object type is used to configure agent virtual machine resource   configuration, such as what network and datastore to use for agent virtual   machines.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='configInfo'>configInfo</a> | [vim.host.EsxAgentHostManager.ConfigInfo](vim.host.EsxAgentHostManager.ConfigInfo.md "vim.host.EsxAgentHostManager.ConfigInfo") | None | Host.Config.Settings | Configuration of agent virtual machine resources |


EsxAgentHostManagerUpdateConfig([configInfo](vim.host.EsxAgentHostManager.ConfigInfo.md "vim.host.EsxAgentHostManager.ConfigInfo"))
-----------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | EsxAgentHostManagerUpdateConfig |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version7) |
| privilege    | Host.Config.Settings |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if an error occurs. |




