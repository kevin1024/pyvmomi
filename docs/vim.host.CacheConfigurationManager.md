vim.host.CacheConfigurationManager
==================================
as of [vSphere API 5.0](vim.version.md#vim.version.version7)
### DEPRECATED



Solid state drive Cache Configuration Manager.    This is a managed object which provides access to ESX performance tuning   features using solid state drive based cache.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='cacheConfigurationInfo'>cacheConfigurationInfo</a> | [vim.host.CacheConfigurationManager.CacheConfigurationInfo](vim.host.CacheConfigurationManager.CacheConfigurationInfo.md "vim.host.CacheConfigurationManager.CacheConfigurationInfo") | true | Host.Config.AdvancedConfig | The swap performance configuration for the ESX host.  This includes  configuration information for each datastore enabled for this purpose. |


ConfigureHostCache([spec](vim.host.CacheConfigurationManager.CacheConfigurationSpec.md "vim.host.CacheConfigurationManager.CacheConfigurationSpec"))
----------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.SystemError](vmodl.fault.SystemError.md "vmodl.fault.SystemError")

---
| service name | ConfigureHostCache |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version7) |
| privilege    | Host.Config.AdvancedConfig |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if swap cache is not supported on this datastore,                          or if swapSize is negative. |
| [vmodl.fault.SystemError](vmodl.fault.SystemError.md "vmodl.fault.SystemError") | if the operation fails due to unexpected reason,                      i.e.: out of disk space situation. |




