vim.dvs.VmwareDistributedVirtualSwitch.LagIpfixConfig
=====================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This class defines the ipfix configuration of the Link Aggregation   Control Protocol group.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ipfixEnabled | bool | true | None | True if ipfix monitoring is enabled in the Link Aggregation Control Protocol group.   If set, this property will override the ipfix configuration of Uplink Ports   in the Link Aggregation Control Protocol group.   Thus they are no longer inheriting ipfix configuration from their Uplink Port Group.   Setting this property would require   <a href="vim.dvs.VmwareDistributedVirtualSwitch.VMwarePortgroupPolicy.md#ipfixOverrideAllowed">ipfixOverrideAllowed</a>   of all the Uplink Port Groups to be true,   otherwise ConflictingConfiguration fault will be raised. |


