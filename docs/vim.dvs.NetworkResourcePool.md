vim.dvs.NetworkResourcePool
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


The <a href="vim.dvs.NetworkResourcePool.md">DVSNetworkResourcePool</a> data object   describes the resource configuration and management   of network resource pools.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Key of the network resource pool. |
| name | string | true | None | Name of the network resource pool. |
| description | string | true | None | Description of the network resource pool. |
| configVersion | string | None | None | Configuration version for the network resource pool. |
| allocationInfo | [vim.dvs.NetworkResourcePool.AllocationInfo](vim.dvs.NetworkResourcePool.AllocationInfo.md "vim.dvs.NetworkResourcePool.AllocationInfo") | None | None | Resource settings of the resource pool. |


