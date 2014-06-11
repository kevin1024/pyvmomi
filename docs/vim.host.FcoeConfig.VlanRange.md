vim.host.FcoeConfig.VlanRange
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Used to represent inclusive intervals of VLAN IDs.   Valid VLAN IDs fall within the range [0,4094], and the low value of a  VlanRange must be less than or equal to the high value.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vlanLow | int | None | None |  |
| vlanHigh | int | None | None |  |


