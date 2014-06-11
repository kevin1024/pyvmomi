vim.host.FcoeConfig.FcoeSpecification
=====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


An FcoeSpecification contains values relevant to issuing FCoE discovery.  Non-mandatory values are denoted '@optional'.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| underlyingPnic | string | None | None | The name of this FcoeSpecification's underlying PhysicalNic |
| priorityClass | int | true | None | 802.1p priority class to use for FCoE traffic. |
| sourceMac | string | true | None | Source MAC address to use for FCoE traffic.   This MAC address is associated with the logical construct that is a  physical NIC's associated underlying FCoE Controller, as defined in  the FC-BB-5 standard.   This MAC address should be of the form "xx:xx:xx:xx:xx:xx", where 'x'  is a hexadecimal digit.  Valid MAC addresses are unicast addresses. |
| vlanRange | [vim.host.FcoeConfig.VlanRange](vim.host.FcoeConfig.VlanRange.md "vim.host.FcoeConfig.VlanRange") | true | None | VLAN ranges to use for FCoE traffic. |


