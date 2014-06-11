vim.DistributedVirtualSwitch.ConfigSpec
=======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.DistributedVirtualSwitch.ConfigSpec.md">DVSConfigSpec</a>  data object contains configuration data for a  <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>.  Use the <a href="vim.DistributedVirtualSwitch.md#reconfigure">ReconfigureDvs_Task</a>  method to apply the configuration to the  switch.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| configVersion | string | true | None | The version string of the configuration that this spec is trying to   change. This property is required in reconfiguring a switch   and should be set to the same value as   <a href="vim.DistributedVirtualSwitch.ConfigInfo.md#configVersion">configVersion</a>.   This property is ignored during switch creation. |
| name | string | true | None | The name of the switch. Must be unique in the parent folder. |
| numStandalonePorts | int | true | None | The number of standalone ports in the switch. Standalone ports are   ports that do not belong to any portgroup. If set to a number larger   than number of existing standalone ports in the switch, new ports get   created to meet the number. If set to a number smaller than the number   of existing standalone ports, free ports (uplink ports excluded) are   deleted to meet the number. If the set number cannot be met by   deleting free standalone ports, a fault is raised. |
| maxPorts | int | true | None | The maximum number of DistributedVirtualPorts allowed in the switch.   If specified in a reconfigure operation, this number cannot be smaller   than the number of existing DistributedVirtualPorts. |
| uplinkPortPolicy | [vim.DistributedVirtualSwitch.UplinkPortPolicy](vim.DistributedVirtualSwitch.UplinkPortPolicy.md "vim.DistributedVirtualSwitch.UplinkPortPolicy") | true | None | The uplink port policy. |
| uplinkPortgroup | [vim.dvs.DistributedVirtualPortgroup](vim.dvs.DistributedVirtualPortgroup.md "vim.dvs.DistributedVirtualPortgroup") | true | None | The uplink portgroups. |
| defaultPortConfig | [vim.dvs.DistributedVirtualPort.Setting](vim.dvs.DistributedVirtualPort.Setting.md "vim.dvs.DistributedVirtualPort.Setting") | true | None | The default configuration for ports. |
| host | [vim.dvs.HostMember.ConfigSpec](vim.dvs.HostMember.ConfigSpec.md "vim.dvs.HostMember.ConfigSpec") | true | None | The host member specification. A particular host should have only one entry   in this array. Duplicate entries for the same host will raise a fault.   The host version should be compatible with the version of   <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>. Use   <a href="vim.dvs.DistributedVirtualSwitchManager.md#checkCompatibility">QueryDvsCheckCompatibility</a>   to check for compatibility. |
| extensionKey | string | true | None | The key of the extension registered by a remote server that   controls the switch. |
| description | string | true | None | Set the description string of the switch. |
| policy | [vim.DistributedVirtualSwitch.SwitchPolicy](vim.DistributedVirtualSwitch.SwitchPolicy.md "vim.DistributedVirtualSwitch.SwitchPolicy") | true | None | The usage policy of the switch. |
| vendorSpecificConfig | [vim.dvs.KeyedOpaqueBlob](vim.dvs.KeyedOpaqueBlob.md "vim.dvs.KeyedOpaqueBlob") | true | None | Set the opaque blob that stores vendor specific configuration. |
| contact | [vim.DistributedVirtualSwitch.ContactInfo](vim.DistributedVirtualSwitch.ContactInfo.md "vim.DistributedVirtualSwitch.ContactInfo") | true | None | Set the human operator contact information. |
| switchIpAddress | string | true | None | IP address for the switch, specified using IPv4 dot notation. The   utility of this address is defined by other switch features. |
| defaultProxySwitchMaxNumPorts | int | true | None | The default host proxy switch maximum port number |


