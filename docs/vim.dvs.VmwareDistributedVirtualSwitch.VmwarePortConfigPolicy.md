vim.dvs.VmwareDistributedVirtualSwitch.VmwarePortConfigPolicy
=============================================================
inherits from [vim.dvs.DistributedVirtualPort.Setting](docs/vim.dvs.DistributedVirtualPort.Setting.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This class defines the VMware specific configuration for   DistributedVirtualPort.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vlan | [vim.dvs.VmwareDistributedVirtualSwitch.VlanSpec](vim.dvs.VmwareDistributedVirtualSwitch.VlanSpec.md "vim.dvs.VmwareDistributedVirtualSwitch.VlanSpec") | true | None | The VLAN Specification of the port. |
| qosTag | [vim.IntPolicy](vim.IntPolicy.md "vim.IntPolicy") | true | None | deprecated  As of vSphere API 5.0 |
| uplinkTeamingPolicy | [vim.dvs.VmwareDistributedVirtualSwitch.UplinkPortTeamingPolicy](vim.dvs.VmwareDistributedVirtualSwitch.UplinkPortTeamingPolicy.md "vim.dvs.VmwareDistributedVirtualSwitch.UplinkPortTeamingPolicy") | true | None | The uplink teaming policy. This property is ignored for uplink   ports. |
| securityPolicy | [vim.dvs.VmwareDistributedVirtualSwitch.SecurityPolicy](vim.dvs.VmwareDistributedVirtualSwitch.SecurityPolicy.md "vim.dvs.VmwareDistributedVirtualSwitch.SecurityPolicy") | true | None | The security policy. |
| ipfixEnabled | [vim.BoolPolicy](vim.BoolPolicy.md "vim.BoolPolicy") | true | None | True if ipfix monitoring is enabled. To successfully enable ipfix   monitoring, the switch must have an assigned   <a href="vim.DistributedVirtualSwitch.ConfigInfo.md#switchIpAddress">IP address</a>   and an appropriately populated   <a href="vim.dvs.VmwareDistributedVirtualSwitch.ConfigInfo.md#ipfixConfig">ipfix configuration</a>   that specifies a collector IP address and port. |
| txUplink | [vim.BoolPolicy](vim.BoolPolicy.md "vim.BoolPolicy") | true | None | If true, a copy of packets sent to the switch will always be forwarded to    an uplink in addition to the regular packet forwarded done by the switch. |
| lacpPolicy | [vim.dvs.VmwareDistributedVirtualSwitch.UplinkLacpPolicy](vim.dvs.VmwareDistributedVirtualSwitch.UplinkLacpPolicy.md "vim.dvs.VmwareDistributedVirtualSwitch.UplinkLacpPolicy") | true | None | Link Aggregation Control Protocol policy.   This policy is ignored on non-uplink portgroups.   Setting this policy at port level is not supported. |


