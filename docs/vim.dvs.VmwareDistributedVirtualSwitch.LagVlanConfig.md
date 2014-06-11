vim.dvs.VmwareDistributedVirtualSwitch.LagVlanConfig
====================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This class defines the vlan configuration of the Link Aggregation   Control Protocol group.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vlanId | [vim.NumericRange](vim.NumericRange.md "vim.NumericRange") | true | None | The VlanId range for the Uplink Ports in the Link Aggregation   Control Protocol group.   The valid VlanId range is from 0 to 4094. Overlapping ranges are allowed.   If set, this property will override the VLAN configuration of Uplink Ports   in the Link Aggregation Control Protocol group.   Thus they are no longer inheriting VLAN configuration from their Uplink Port Group.   Setting this property would require   <a href="vim.dvs.VmwareDistributedVirtualSwitch.VMwarePortgroupPolicy.md#vlanOverrideAllowed">vlanOverrideAllowed</a>   of all the Uplink Port Groups to be true,   otherwise ConflictingConfiguration fault will be raised. |


