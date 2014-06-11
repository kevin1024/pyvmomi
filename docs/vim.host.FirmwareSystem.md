vim.host.FirmwareSystem
=======================
as of [VI API 2.5](vim.version.md#vim.version.version2)


The <a href="vim.host.FirmwareSystem.md">HostFirmwareSystem</a> managed object type provides access to the firmware   of an embedded ESX host. It provides operations to backup, restore, and reset the   configuration of an embedded ESX host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


ResetFirmwareToFactoryDefaults()
--------------------------------
 raises [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | ResetFirmwareToFactoryDefaults |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | Host.Config.Firmware |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the host is not in maintenance mode. |




BackupFirmwareConfiguration()
-----------------------------

| service name | BackupFirmwareConfiguration |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | Host.Config.Firmware |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|




QueryFirmwareConfigUploadURL()
------------------------------

| service name | QueryFirmwareConfigUploadURL |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | Host.Config.Firmware |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|




RestoreFirmwareConfiguration()
------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidBundle](vim.fault.InvalidBundle.md "vim.fault.InvalidBundle"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.MismatchedBundle](vim.fault.MismatchedBundle.md "vim.fault.MismatchedBundle")

---
| service name | RestoreFirmwareConfiguration |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | Host.Config.Firmware |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the host is not in maintenance mode. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if the file was not accessible. |
| [vim.fault.MismatchedBundle](vim.fault.MismatchedBundle.md "vim.fault.MismatchedBundle") | if the uuid / build number in the bundle          does not match the uuid / build number of the host and          parameter 'force' is set to false. |
| [vim.fault.InvalidBundle](vim.fault.InvalidBundle.md "vim.fault.InvalidBundle") | if the bundle does not have the expected contents. |




