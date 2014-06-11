vim.host.FcoeConfig
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


This data object type describes an FCoE configuration as it pertains   to an underlying physical NIC.    Terminology is borrowed from T11's working draft of the Fibre Channel   Backbone 5 standard (FC-BB-5).  The draft can be found at   http://www.t11.org.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| priorityClass | int | None | None | 802.1p priority class used for FCoE traffic. |
| sourceMac | string | None | None | Source MAC address used for FCoE traffic.   This MAC address is associated with the logical construct that is a  physical NIC's associated underlying FCoE Controller, as defined in the  FC-BB-5 standard.   This MAC address should be of the form "xx:xx:xx:xx:xx:xx", where 'x' is  a hexadecimal digit.  Valid MAC addresses are unicast addresses. |
| vlanRange | [vim.host.FcoeConfig.VlanRange](vim.host.FcoeConfig.VlanRange.md "vim.host.FcoeConfig.VlanRange") | None | None | VLAN ranges associated with this FcoeConfig. |
| capabilities | [vim.host.FcoeConfig.FcoeCapabilities](vim.host.FcoeConfig.FcoeCapabilities.md "vim.host.FcoeConfig.FcoeCapabilities") | None | None | Settable capabilities for this FcoeConfig. |
| fcoeActive | bool | None | None | Indicates whether this FcoeConfig is "active" (has been used in  conjunction with a parent physical network adapter for FCoE  discovery). |


