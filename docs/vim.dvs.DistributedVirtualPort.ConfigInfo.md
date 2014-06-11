vim.dvs.DistributedVirtualPort.ConfigInfo
=========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Management related configuration of a DistributedVirtualPort.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | true | None | The name of the port. |
| scope | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | true | None | The eligible entities that can connect to the port. If unset, there   is no restriction on which entity can connect to the port. If set,   only the entities in the specified list or their child entities are   allowed to connect to the port. If scopes are defined at both port   and portgroup level, they are taken as an "AND" relationship. If such   a relationship doesn't make sense, the reconfigure operation will   raise an exception. |
| description | string | true | None | A description string of the port. |
| setting | [vim.dvs.DistributedVirtualPort.Setting](vim.dvs.DistributedVirtualPort.Setting.md "vim.dvs.DistributedVirtualPort.Setting") | true | None | The network configuration of the port. |
| configVersion | string | None | None | The version string of the configuration. |


