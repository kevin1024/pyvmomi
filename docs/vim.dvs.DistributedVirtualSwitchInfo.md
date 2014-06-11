vim.dvs.DistributedVirtualSwitchInfo
====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This class describes a DistributedVirtualSwitch that a device backing   can attached to its ports.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| switchName | string | None | None | The name of the switch. |
| switchUuid | string | None | None | The UUID of the switch. |
| distributedVirtualSwitch | [vim.DistributedVirtualSwitch](vim.DistributedVirtualSwitch.md "vim.DistributedVirtualSwitch") | None | None | The switch. |


