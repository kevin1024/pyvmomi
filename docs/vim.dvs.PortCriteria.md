vim.dvs.PortCriteria
====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The criteria specification for selecting ports.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| connected | bool | true | None | If set, only the connected ports are qualified. |
| active | bool | true | None | If set, only the active ports are qualified. |
| uplinkPort | bool | true | None | If set to true, only the uplink ports are qualified. If set to false, only   non-uplink ports are qualified. |
| scope | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | true | None | If set, only the ports of which the scope covers the entity are   qualified. |
| portgroupKey | string | true | None | The keys of the portgroup that is used for the scope of <a href="vim.dvs.PortCriteria.md#inside">inside</a>.   If this property is unset, it means any portgroup. If <a href="vim.dvs.PortCriteria.md#inside">inside</a>   is unset, this property is ignored. |
| inside | bool | true | None | If unset, all ports in the switch are qualified.   If set to true, only ports inside <a href="vim.dvs.PortCriteria.md#portgroupKey">portgroupKey</a> or any   portgroup, if not set, are qualified.   If set to false, only ports outside <a href="vim.dvs.PortCriteria.md#portgroupKey">portgroupKey</a> or any   portgroup, if not set, are qualified. |
| portKey | string | true | None | If set, only the ports of which the key is in the array are   qualified. |


