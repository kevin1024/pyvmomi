vim.dvs.DistributedVirtualPortgroup.ConfigSpec
==============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.dvs.DistributedVirtualPortgroup.ConfigSpec.md">DVPortgroupConfigSpec</a>  data object contains configuration data for a  <a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a>. Use the  <a href="vim.dvs.DistributedVirtualPortgroup.md#reconfigure">ReconfigureDVPortgroup_Task</a>  method to apply the configuration to the portgroup.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| configVersion | string | true | None | Version string of the configuration that this spec is trying to   change. This property is required in reconfiguring a portgroup and   should be set to the same value as the   <a href="vim.dvs.DistributedVirtualPortgroup.ConfigInfo.md#configVersion">configVersion</a>.   This property is ignored in creating a portgroup if set. |
| name | string | true | None | Name of the portgroup. |
| numPorts | int | true | None | Number of ports in the portgroup. Setting this number larger than the   number of existing ports in the portgroup causes new ports to   be added to the portgroup to meet the number. Setting this property   smaller than the number of existing ports deletes the free ports   from the portgroup. If the number cannot be met by deleting free ports,   a fault is raised.  If new ports are added to the portgroup, they   are also added to the switch. For portgroups of type ephemeral this   property is ignored. |
| portNameFormat | string | true | None | Format of the name of the ports when ports are created in the portgroup.   For details see <a href="vim.dvs.DistributedVirtualPortgroup.ConfigInfo.md#portNameFormat">portNameFormat</a>. |
| defaultPortConfig | [vim.dvs.DistributedVirtualPort.Setting](vim.dvs.DistributedVirtualPort.Setting.md "vim.dvs.DistributedVirtualPort.Setting") | true | None | Default network setting for all the ports in the portgroup. |
| description | string | true | None | Description of the portgroup. |
| type | string | true | None | Type of portgroup.  See  <a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a>.<a href="vim.dvs.DistributedVirtualPortgroup.PortgroupType.md">DistributedVirtualPortgroupPortgroupType</a>  for possible values. |
| scope | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | true | None | Eligible entities that can connect to the port. See  <a href="vim.dvs.DistributedVirtualPortgroup.ConfigInfo.md">DVPortgroupConfigInfo</a>.<a href="vim.dvs.DistributedVirtualPortgroup.ConfigInfo.md#scope">scope</a>. |
| policy | [vim.dvs.DistributedVirtualPortgroup.PortgroupPolicy](vim.dvs.DistributedVirtualPortgroup.PortgroupPolicy.md "vim.dvs.DistributedVirtualPortgroup.PortgroupPolicy") | true | None | Portgroup policy. |
| vendorSpecificConfig | [vim.dvs.KeyedOpaqueBlob](vim.dvs.KeyedOpaqueBlob.md "vim.dvs.KeyedOpaqueBlob") | true | None | Opaque binary blob that stores vendor specific configuration. |
| autoExpand | bool | true | None | If set to true, this property ignores the limit on the number of ports in the   portgroup. When a Virtual Machine/Host tries to connect to the portgroup and there   are no free ports available in the portgroup, new ports will be automatically   added to the portgroup. The flag is currently supported only for static portgroups.   <p>   Setting this property to true makes the portgroup a potential candidate for   auto-shrink. Once the portgroup has auto-expanded then its disconnected ports are   likely to be deleted automatically, as a part of auto-shrink step, if there are more   than certain number of free ports. If the portgroup never auto-expanded, then it will   never lose any free ports. |


