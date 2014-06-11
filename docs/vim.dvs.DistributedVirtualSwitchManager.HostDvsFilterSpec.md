vim.dvs.DistributedVirtualSwitchManager.HostDvsFilterSpec
=========================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Base class for filters to check host compatibility.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| inclusive | bool | None | None | If this flag is true, then the filter returns the hosts in the  <a href="vim.dvs.DistributedVirtualSwitchManager.HostContainer.md">DistributedVirtualSwitchManagerHostContainer</a>  that satisfy the criteria specified by this filter, otherwise  it returns hosts that don't meet the criteria. |


