vim.host.PowerSystem
====================
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Managed object responsible for getting and setting host    power management policies.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='capability'>capability</a> | [vim.host.PowerSystem.Capability](vim.host.PowerSystem.Capability.md "vim.host.PowerSystem.Capability") | None | Host.Config.Power | Power system capabilities object. |
| <a href='info'>info</a> | [vim.host.PowerSystem.Info](vim.host.PowerSystem.Info.md "vim.host.PowerSystem.Info") | None | Host.Config.Power | Power system state info object. |


ConfigurePowerPolicy()
----------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | ConfigurePowerPolicy |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version6) |
| privilege    | Host.Config.Power |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for any other failure. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if an invalid power policy key is provided. |




