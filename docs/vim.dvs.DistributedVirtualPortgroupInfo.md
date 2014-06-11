vim.dvs.DistributedVirtualPortgroupInfo
=======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This class describes a DistributedVirtualPortgroup that a device backing   can be attached to.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| switchName | string | None | None | The name of the switch. |
| switchUuid | string | None | None | The UUID of the switch. |
| portgroupName | string | None | None | The name of the portgroup. |
| portgroupKey | string | None | None | The key of the portgroup. |
| portgroupType | string | None | None | The type of portgroup.   See <a href="vim.dvs.DistributedVirtualPortgroup.PortgroupType.md">DistributedVirtualPortgroupPortgroupType</a> |
| uplinkPortgroup | bool | None | None | Whether this portgroup is an uplink portgroup. |
| portgroup | [vim.dvs.DistributedVirtualPortgroup](vim.dvs.DistributedVirtualPortgroup.md "vim.dvs.DistributedVirtualPortgroup") | None | None | The portgroup. |


