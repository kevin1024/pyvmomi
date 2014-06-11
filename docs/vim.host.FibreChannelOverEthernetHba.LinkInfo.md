vim.host.FibreChannelOverEthernetHba.LinkInfo
=============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Represents FCoE link information.   The link information represents a VNPort to VFPort Virtual Link, as  described in the FC-BB-5 standard, with the addition of the VLAN ID  over which a link exists.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vnportMac | string | None | None | VNPort MAC address, as defined by the FC-BB-5 standard.   This MAC address should be of the form "xx:xx:xx:xx:xx:xx", where  'x' is a hexadecimal digit.  Valid MAC addresses are unicast  addresses. |
| fcfMac | string | None | None | FCF MAC address, also known as the VFPort MAC address in the FC-BB-5  standard.   This MAC address should be of the form "xx:xx:xx:xx:xx:xx", where  'x' is a hexadecimal digit.  Valid MAC addresses are unicast  addresses. |
| vlanId | int | None | None | VLAN ID.   This field represents the VLAN on which an FCoE HBA was  discovered.  Valid numbers fall into the range [0,4094]. |


