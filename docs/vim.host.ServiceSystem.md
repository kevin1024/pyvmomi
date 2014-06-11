vim.host.ServiceSystem
======================
inherits from [vim.ExtensibleManagedObject](vim.ExtensibleManagedObject.md "vim.ExtensibleManagedObject")


The <a href="vim.host.ServiceSystem.md">HostServiceSystem</a> managed object describes the configuration   of host services.  This managed object operates in conjunction   with the <a href="vim.host.FirewallSystem.md">HostFirewallSystem</a>   managed object.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='serviceInfo'>serviceInfo</a> | [vim.host.ServiceInfo](vim.host.ServiceInfo.md "vim.host.ServiceInfo") | None | None | Service configuration. |


UpdateServicePolicy([id](#string "string"), [policy](#string "string"))
-----------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UpdateServicePolicy |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.NetService |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the service ID is unknown. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other failures. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the service ID represents a required service,   or if the specified policy is undefined. |




StartService([id](#string "string"))
------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | StartService |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.NetService |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the service is already running.           Only hosts with ESX/ESXi 4.1 or earlier software use this fault.           Hosts running later versions of ESXi do not throw a fault in this case. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the service ID is unknown. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other failures. |




StopService([id](#string "string"))
-----------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | StopService |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.NetService |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the service is not running.           Only hosts with ESX/ESXi 4.1 or earlier software use this fault.           Hosts running later versions of ESXi do not throw a fault in this case. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the service ID is unknown. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other failures. |




RestartService([id](#string "string"))
--------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | RestartService |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.NetService |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the service is not running.           Only hosts with ESX/ESXi 4.1 or earlier software use this fault.           Hosts running later versions of ESXi do not throw a fault in this case. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the service ID is unknown. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other failures. |




UninstallService([id](#string "string"))
----------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UninstallService |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.NetService |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the service ID is unknown. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other failures. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the service is a required service. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the service doesn't support uninstallation. |




RefreshServices()
-----------------

| service name | RefreshServices |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.NetService |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




