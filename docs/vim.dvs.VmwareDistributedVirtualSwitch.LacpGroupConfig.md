vim.dvs.VmwareDistributedVirtualSwitch.LacpGroupConfig
======================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This class defines VMware specific multiple IEEE 802.3ad   Dynamic Link Aggregation Control Protocol groups.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | true | None | The generated key as the identifier for the Link Aggregation group. |
| name | string | true | None | The display name. |
| mode | string | true | None | The mode of Link Aggregation Control Protocol.   See UplinkLacpMode for valid values. |
| uplinkNum | int | true | None | The number of uplink ports. |
| loadbalanceAlgorithm | string | true | None | Load balance policy.   See LacpLoadBalanceAlgorithm for valid values. |
| vlan | [vim.dvs.VmwareDistributedVirtualSwitch.LagVlanConfig](vim.dvs.VmwareDistributedVirtualSwitch.LagVlanConfig.md "vim.dvs.VmwareDistributedVirtualSwitch.LagVlanConfig") | true | None | The VLAN Specification of the Uplink Ports in the Link Aggregation group. |
| ipfix | [vim.dvs.VmwareDistributedVirtualSwitch.LagIpfixConfig](vim.dvs.VmwareDistributedVirtualSwitch.LagIpfixConfig.md "vim.dvs.VmwareDistributedVirtualSwitch.LagIpfixConfig") | true | None | Ipfix configuration of the Link Aggregation   Control Protocol group. |
| uplinkName | string | true | None | Names for the Uplink Ports in the group.   This property is ignored in an update operation. |
| uplinkPortKey | string | true | None | Keys for the Uplink Ports in the group.   This property is ignored in an update operation. |


