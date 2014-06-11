vim.host.HardwareStatusInfo.HardwareElementInfo
===============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


Data object describing the operational status of a physical   element.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | The name of the physical element |
| status | [vim.ElementDescription](vim.ElementDescription.md "vim.ElementDescription") | None | None | The operational status of the physical element. The status is one of   the values specified in HostHardwareElementStatus.<br>See <a href="vim.host.HardwareStatusInfo.Status.md">HostHardwareElementStatus</a><br> |


