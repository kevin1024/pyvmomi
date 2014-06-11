vim.host.BootDeviceSystem
=========================
as of [VI API 2.5](vim.version.md#vim.version.version2)


The <a href="vim.host.BootDeviceSystem.md">HostBootDeviceSystem</a> managed object provides methods to query and update   a host boot device configuration.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


QueryBootDevices()
------------------

| service name | QueryBootDevices |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




UpdateBootDevice([key](#string "string"))
-----------------------------------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | UpdateBootDevice |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | Host.Config.Maintenance |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host does not support updating bootDevices. |




