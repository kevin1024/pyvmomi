vim.host.SnmpSystem
===================


Provision the SNMP Version 1,2c agent.   This object is accessed through the  <a href="vim.host.ConfigManager.md">HostConfigManager</a> object.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='configuration'>configuration</a> | [vim.host.SnmpSystem.SnmpConfigSpec](vim.host.SnmpSystem.SnmpConfigSpec.md "vim.host.SnmpSystem.SnmpConfigSpec") | None | Global.Settings |  |
| <a href='limits'>limits</a> | [vim.host.SnmpSystem.AgentLimits](vim.host.SnmpSystem.AgentLimits.md "vim.host.SnmpSystem.AgentLimits") | None | Global.Settings |  |


ReconfigureSnmpAgent([spec](vim.host.SnmpSystem.SnmpConfigSpec.md "vim.host.SnmpSystem.SnmpConfigSpec"))
--------------------------------------------------------------------------------------------------------
 raises [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | ReconfigureSnmpAgent |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | Global.Settings |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | vim.fault.NotFound |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | vim.fault.InsufficientResourcesFault |




SendTestNotification()
----------------------
 raises [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | SendTestNotification |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | Global.Settings |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | vim.fault.NotFound |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | vim.fault.InsufficientResourcesFault |




