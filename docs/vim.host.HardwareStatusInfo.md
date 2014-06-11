vim.host.HardwareStatusInfo
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


Data object representing the status of the   hardware components of the host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| memoryStatusInfo | [vim.host.HardwareStatusInfo.HardwareElementInfo](vim.host.HardwareStatusInfo.HardwareElementInfo.md "vim.host.HardwareStatusInfo.HardwareElementInfo") | true | None | Status of the physical memory |
| cpuStatusInfo | [vim.host.HardwareStatusInfo.HardwareElementInfo](vim.host.HardwareStatusInfo.HardwareElementInfo.md "vim.host.HardwareStatusInfo.HardwareElementInfo") | true | None | Status of the CPU packages |
| storageStatusInfo | [vim.host.HardwareStatusInfo.StorageStatusInfo](vim.host.HardwareStatusInfo.StorageStatusInfo.md "vim.host.HardwareStatusInfo.StorageStatusInfo") | true | None | Status of the physical storage system |


