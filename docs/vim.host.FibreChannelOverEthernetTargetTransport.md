vim.host.FibreChannelOverEthernetTargetTransport
================================================
inherits from [vim.host.FibreChannelTargetTransport](docs/vim.host.FibreChannelTargetTransport.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Fibre Channel Over Ethernet transport information about a SCSI target.    FCoE transport information is that of: the regular FC World Wide Node   and Port Names; the VNPort MAC address and FCF MAC address which   constitute a VN_Port to VF_Port Virtual Link; and the VLAN on which   an FCoE target resides.    More FCoE information can be found in the working draft of the T11's   Fibre Channel Backbone 5 standard (FC-BB-5).  The draft can be found   at http://www.t11.org.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vnportMac | string | None | None | VNPort MAC address.   This MAC address should be of the form "xx:xx:xx:xx:xx:xx", where  'x' is a hexadecimal digit.  Valid MAC addresses are unicast  addresses. |
| fcfMac | string | None | None | FCF MAC address.   This MAC address should be of the form "xx:xx:xx:xx:xx:xx", where  'x' is a hexadecimal digit.  Valid MAC addresses are unicast  addresses. |
| vlanId | int | None | None | VLAN ID.   Valid VLAN IDs fall within the range [0,4094]. |


