vim.host.PciPassthruSystem
==========================
inherits from [vim.ExtensibleManagedObject](vim.ExtensibleManagedObject.md "vim.ExtensibleManagedObject")
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This managed object manages the PciPassthru state of the host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='pciPassthruInfo'>pciPassthruInfo</a> | [vim.host.PciPassthruInfo](vim.host.PciPassthruInfo.md "vim.host.PciPassthruInfo") | None | System.Read | Array of PciPassthru information |


Refresh()
---------

| service name | Refresh |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | Host.Config.Settings |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




UpdatePassthruConfig([config](vim.host.PciPassthruConfig.md "vim.host.PciPassthruConfig"))
------------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | UpdatePassthruConfig |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | Host.Config.PciPassthru |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if an error occurs. |




