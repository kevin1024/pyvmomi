vim.dvs.NetworkResourcePool.AllocationInfo
==========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Resource allocation information for a network resource pool.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| limit | long | true | None | Maximum allowed usage for network clients belonging to   this resource pool per host.   The utilization of network clients belonging to this resource pool   will not exceed the specified limit even if there are available   network resources. If set to -1, then there is no limit on the network   resource usage for clients belonging to this resource pool. Units are   in Mbits/sec. When setting the allocation of a particular resource   pool, if the property is unset, it is treated as no change and the   property is not updated. An unset limit value while reading back the   allocation information of a network resource pool indicates that   there is no limit on the network resource usage for the clients   belonging to this resource group. |
| shares | [vim.SharesInfo](vim.SharesInfo.md "vim.SharesInfo") | true | None | Share settings associated with the network resource pool to   facilitate proportional sharing of the physical network resources.   If the property is unset when setting the allocation of a particular   resource pool, it is treated as unset and the property is not updated.   The property is always set when reading back the allocation   information of a network resource pool. |
| priorityTag | int | true | None | 802.1p tag to be used for this resource pool. The tag is a priority value  in the range 0..7 for Quality of Service operations on network traffic. |


