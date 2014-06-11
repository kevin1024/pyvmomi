vim.dvs.DistributedVirtualPortgroup.ConfigInfo
==============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.dvs.DistributedVirtualPortgroup.ConfigInfo.md">DVPortgroupConfigInfo</a> data object defines  the configuration of a <a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a>.   .

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Key of the portgroup. |
| name | string | None | None | Name of the portgroup. |
| numPorts | int | None | None | Number of ports in the portgroup. |
| distributedVirtualSwitch | [vim.DistributedVirtualSwitch](vim.DistributedVirtualSwitch.md "vim.DistributedVirtualSwitch") | true | None | Distributed virtual switch that the portgroup is defined on.  This property should always be set unless the user's setting  does not have System.Read privilege on the object referred to  by this property. |
| defaultPortConfig | [vim.dvs.DistributedVirtualPort.Setting](vim.dvs.DistributedVirtualPort.Setting.md "vim.dvs.DistributedVirtualPort.Setting") | true | None | Common network setting for all the ports in the portgroup. |
| description | string | true | None | Description of the portgroup. |
| type | string | None | None | Type of portgroup. See  <a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a>.<a href="vim.dvs.DistributedVirtualPortgroup.PortgroupType.md">DistributedVirtualPortgroupPortgroupType</a>  for possible values. |
| policy | [vim.dvs.DistributedVirtualPortgroup.PortgroupPolicy](vim.dvs.DistributedVirtualPortgroup.PortgroupPolicy.md "vim.dvs.DistributedVirtualPortgroup.PortgroupPolicy") | None | None | Portgroup policy. |
| portNameFormat | string | true | None | If set, a name will be automatically generated based on this format   string for a port when it is created in or moved into the portgroup.   The format string can contain meta tags that will be resolved   to the corresponding values in generating a name, if applicable for   the port at the time of name generation.   <p>   To insert a meta tag in the format string,   enclose the names defined as meta tag names inside angle brackets.   See <a href="vim.dvs.DistributedVirtualPortgroup.MetaTagName.md">DistributedVirtualPortgroupMetaTagName</a> for a list of   currently available meta tags.  For example,   "redNetwork-&lt;portIndex&gt;" and "&lt;dvsName&gt;-pnic&lt;portIndex&gt;"   result in generated port names like "redNetwork-2" and "switch-pnic3".   <p>   If a meta tag is recognized, but there is no applicable value, the tag   will be expanded to empty string. If an arbitrary name appears inside   a "&lt;&gt;" pair and is not recognized as one of the defined meta tags,   the substring is treated as-is and appear unchanged in the generated name.   <p>   To prevent a meta tag from being expanded, prefix the meta tag with a   '\' (backslash). For example, the format string "abc\&lt;portIndex&gt;def"   results in the generated port name "abc&lt;portIndex&gt;def". |
| scope | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | true | None | Eligible entities that can connect to the portgroup. If unset,   there is no restriction on which entity can connect to the portgroup.   If set, only the entities in the specified list or their child   entities are allowed to connect to the portgroup. If scopes are   defined at both port and portgroup level, they are taken as an "AND"   relationship. If such a relationship doesn't make sense, the   reconfigure operation will raise an exception. |
| vendorSpecificConfig | [vim.dvs.KeyedOpaqueBlob](vim.dvs.KeyedOpaqueBlob.md "vim.dvs.KeyedOpaqueBlob") | true | None | Opaque binary blob that stores vendor specific configuration. |
| configVersion | string | true | None | Configuration version number. |
| autoExpand | bool | true | None | If set to true, this property ignores the limit on the number of ports in the   portgroup. When a Virtual Machine/Host tries to connect to the portgroup and there   are no free ports available in the portgroup, new ports will be automatically   added to the portgroup. The flag is currently supported only for static portgroups.   <p>   When this property is set to true, the portgroup becomes a potential candidate for   auto-shrink. Once the portgroup has auto-expanded then its disconnected ports are   likely to be deleted automatically, as a part of auto-shrink step, if there are more   than certain number of free ports. If the portgroup never auto-expanded, then it will   never lose any free ports. |


