vim.host.VMotionSystem
======================
inherits from [vim.ExtensibleManagedObject](vim.ExtensibleManagedObject.md "vim.ExtensibleManagedObject")
### DEPRECATED



The VMotionSystem managed object describes the VMotion configuration   of the host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='netConfig'>netConfig</a> | [vim.host.VMotionSystem.NetConfig](vim.host.VMotionSystem.NetConfig.md "vim.host.VMotionSystem.NetConfig") | true | None | VMotion network configuration. |
| <a href='ipConfig'>ipConfig</a> | [vim.host.IpConfig](vim.host.IpConfig.md "vim.host.IpConfig") | true | None | IP configuration of the VMotion VirtualNic. |


UpdateIpConfig([ipConfig](vim.host.IpConfig.md "vim.host.IpConfig"))
--------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UpdateIpConfig |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Network |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if no VirtualNic is selected for VMotion. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for any other failure |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the IpConfig is invalid or cannot be used. |




SelectVnic([device](#string "string"))
--------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | SelectVnic |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Network |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for any other failure |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if key represents a nonexistent or invalid VirtualNic. |




DeselectVnic()
--------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | DeselectVnic |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Network |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | is a failure occurred |




