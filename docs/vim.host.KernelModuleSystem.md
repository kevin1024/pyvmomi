vim.host.KernelModuleSystem
===========================
as of [VI API 2.5u2](vim.version.md#vim.version.version3)


The KernelModuleSystem managed object controls the configuration   of kernel modules on the host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


QueryModules()
--------------

| service name | QueryModules |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#vim.version.version3) |
| privilege    | Host.Config.Settings |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




UpdateModuleOptionString([name](#string "string"), [options](#string "string"))
-------------------------------------------------------------------------------
 raises [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UpdateModuleOptionString |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version3) |
| privilege    | Host.Config.Settings |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the kernel module does not exist on the host. |




QueryConfiguredModuleOptionString([name](#string "string"))
-----------------------------------------------------------
 raises [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | QueryConfiguredModuleOptionString |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version3) |
| privilege    | Host.Config.Settings |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the kernel module does not exist on the host. |




