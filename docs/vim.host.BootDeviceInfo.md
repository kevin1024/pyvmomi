vim.host.BootDeviceInfo
=======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This data object represents the boot device information of the host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| bootDevices | [vim.host.BootDeviceSystem.BootDevice](vim.host.BootDeviceSystem.BootDevice.md "vim.host.BootDeviceSystem.BootDevice") | true | None | The list of boot devices present on the host |
| currentBootDeviceKey | string | true | None | The key of the current boot device that the host is configured to    boot. This property is unset if the current boot device is disabled. |


