vim.host.VirtualNicManager
==========================
inherits from [vim.ExtensibleManagedObject](vim.ExtensibleManagedObject.md "vim.ExtensibleManagedObject")
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The VirtualNicManager managed object describes the special Virtual NIC   configuration of the host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='info'>info</a> | [vim.host.VirtualNicManagerInfo](vim.host.VirtualNicManagerInfo.md "vim.host.VirtualNicManagerInfo") | None | None | Network configuration. |


QueryNetConfig([nicType](#string "string"))
-------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | QueryNetConfig |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | Host.Config.Network |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for any other failure. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if nicType is invalid |




SelectVnicForNicType([nicType](#string "string"), [device](#string "string"))
-----------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | SelectVnicForNicType |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | Host.Config.Network |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for any other failure. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if nicType is invalid, or device represents a           nonexistent or invalid VirtualNic |




DeselectVnicForNicType([nicType](#string "string"), [device](#string "string"))
-------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | DeselectVnicForNicType |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | Host.Config.Network |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for any other failure. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if nicType is invalid, device represents           a nonexistent or invalid VirtualNic, or the VirtualNic is           not selected |




