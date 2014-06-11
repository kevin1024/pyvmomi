vim.dvs.VmwareDistributedVirtualSwitch.PvlanMapEntry
====================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The class represents a PVLAN id.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| primaryVlanId | int | None | None | The primary VLAN ID. The VLAN IDs of 0 and 4095 are reserved   and cannot be used in this property. |
| secondaryVlanId | int | None | None | The secondary VLAN ID. The VLAN IDs of 0 and 4095 are reserved   and cannot be used in this property. |
| pvlanType | string | None | None | The type of PVLAN.   See <a href="vim.dvs.VmwareDistributedVirtualSwitch.PvlanPortType.md">VmwareDistributedVirtualSwitchPvlanPortType</a>   for valid values. |


