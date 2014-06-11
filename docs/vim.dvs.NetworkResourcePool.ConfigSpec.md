vim.dvs.NetworkResourcePool.ConfigSpec
======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


The <a href="vim.dvs.NetworkResourcePool.ConfigSpec.md">DVSNetworkResourcePoolConfigSpec</a> data object  contains properties to create or update a network resource pool  for a distributed virtual switch.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Key of the network resource pool. The property is ignored for  <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>.<a href="vim.DistributedVirtualSwitch.md#addNetworkResourcePool">AddNetworkResourcePool</a>  operations. |
| configVersion | string | true | None | Unique identifier for a given version   of the configuration. Each change to the configuration will   update this value. This is typically implemented as a   non-decreasing count or a time-stamp. However, a client should   always treat this as an opaque string.   <p>   If you specify the configuration version when you update   the resource configuration, the Server will apply the changes   only if the specified identifier matches the current   <a href="vim.dvs.NetworkResourcePool.md">DVSNetworkResourcePool</a>.<a href="vim.dvs.NetworkResourcePool.md#configVersion">configVersion</a>   value. You can use this field to guard against updates   that may have occurred between the time when the client   reads <a href="vim.dvs.NetworkResourcePool.md#configVersion">configVersion</a>   and when the configuration is applied. |
| allocationInfo | [vim.dvs.NetworkResourcePool.AllocationInfo](vim.dvs.NetworkResourcePool.AllocationInfo.md "vim.dvs.NetworkResourcePool.AllocationInfo") | true | None | Network resource allocation for the network resource pool. |
| name | string | true | None | User defined name for the resource pool.   The property is required for   <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>.<a href="vim.DistributedVirtualSwitch.md#addNetworkResourcePool">AddNetworkResourcePool</a>   operations. |
| description | string | true | None | User-defined description for the resource pool. |


