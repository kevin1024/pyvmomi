vim.DistributedVirtualSwitch.ConfigInfo
=======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Configuration of a <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| uuid | string | None | None | Generated UUID of the switch. Unique across vCenter Server   inventory and instances. |
| name | string | None | None | Name of the switch. |
| numStandalonePorts | int | None | None | Number of standalone ports in the switch. Standalone ports are   ports that do not belong to any portgroup. |
| numPorts | int | None | None | Current number of ports, not including conflict ports. |
| maxPorts | int | None | None | Maximum number of ports allowed in the switch,   not including conflict ports. |
| uplinkPortPolicy | [vim.DistributedVirtualSwitch.UplinkPortPolicy](vim.DistributedVirtualSwitch.UplinkPortPolicy.md "vim.DistributedVirtualSwitch.UplinkPortPolicy") | None | None | Uplink port policy. |
| uplinkPortgroup | [vim.dvs.DistributedVirtualPortgroup](vim.dvs.DistributedVirtualPortgroup.md "vim.dvs.DistributedVirtualPortgroup") | true | None | List of uplink portgroups. When adding host members, the server   uses the <a href="vim.DistributedVirtualSwitch.ConfigInfo.md#uplinkPortPolicy">uplinkPortPolicy</a> to create a number of   uplink ports for the host. If portgroups are shown here,   those uplink ports will be added to the portgroups, with uplink ports   evenly spread among the portgroups. |
| defaultPortConfig | [vim.dvs.DistributedVirtualPort.Setting](vim.dvs.DistributedVirtualPort.Setting.md "vim.dvs.DistributedVirtualPort.Setting") | None | None | Default configuration for the ports in the switch, if the port   does not inherit configuration from the parent portgroup or has   its own configuration. |
| host | [vim.dvs.HostMember](vim.dvs.HostMember.md "vim.dvs.HostMember") | true | None | Hosts that join the switch. |
| productInfo | [vim.dvs.ProductSpec](vim.dvs.ProductSpec.md "vim.dvs.ProductSpec") | None | None | Vendor, product, and version information for the implementation   module of the switch. |
| targetInfo | [vim.dvs.ProductSpec](vim.dvs.ProductSpec.md "vim.dvs.ProductSpec") | true | None | Intended vendor, product, and version information for the   implementation module of the switch. |
| extensionKey | string | true | None | Key of the extension registered by the remote server that   controls the switch. |
| vendorSpecificConfig | [vim.dvs.KeyedOpaqueBlob](vim.dvs.KeyedOpaqueBlob.md "vim.dvs.KeyedOpaqueBlob") | true | None | Opaque binary blob that stores vendor specific configuration. |
| policy | [vim.DistributedVirtualSwitch.SwitchPolicy](vim.DistributedVirtualSwitch.SwitchPolicy.md "vim.DistributedVirtualSwitch.SwitchPolicy") | true | None | Usage policy of the switch. |
| description | string | true | None | Description string for the switch. |
| configVersion | string | None | None | Version string of the configuration. |
| contact | [vim.DistributedVirtualSwitch.ContactInfo](vim.DistributedVirtualSwitch.ContactInfo.md "vim.DistributedVirtualSwitch.ContactInfo") | None | None | Human operator contact information. |
| switchIpAddress | string | true | None | IP address for the switch, specified using IPv4 dot notation. The   utility of this address is defined by other switch features. |
| createTime | datetime | None | None | Create time of the switch. |
| networkResourceManagementEnabled | bool | None | None | Boolean to indicate if network I/O control is enabled on the   switch. |
| defaultProxySwitchMaxNumPorts | int | true | None | Default host proxy switch maximum port number |
| healthCheckConfig | [vim.DistributedVirtualSwitch.HealthCheckConfig](vim.DistributedVirtualSwitch.HealthCheckConfig.md "vim.DistributedVirtualSwitch.HealthCheckConfig") | true | None | VDS health check configuration. |


