vim.dvs.DistributedVirtualSwitchManager.DvsConfigTarget
=======================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Configuration specification for a DistributedVirtualSwitch or   DistributedVirtualPortgroup.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| distributedVirtualPortgroup | [vim.dvs.DistributedVirtualPortgroupInfo](vim.dvs.DistributedVirtualPortgroupInfo.md "vim.dvs.DistributedVirtualPortgroupInfo") | true | None | List of any DistributedVirtualPortgroup available for host Virtual NIC connection. |
| distributedVirtualSwitch | [vim.dvs.DistributedVirtualSwitchInfo](vim.dvs.DistributedVirtualSwitchInfo.md "vim.dvs.DistributedVirtualSwitchInfo") | true | None | List of any DistributedVirtualSwitch available for host Virtual NIC connection. |


