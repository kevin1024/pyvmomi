vim.host.IpConfig
=================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The IP configuration.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| dhcp | bool | None | None | The flag to indicate whether or not DHCP (dynamic host   control protocol) is enabled.  If this property is set to true,   the ipAddress and the subnetMask strings cannot be set explicitly. |
| ipAddress | string | true | None | The IP address currently used by the network adapter.   All IP addresses are specified using IPv4 dot notation.   For example, "192.168.0.1". Subnet addresses and netmasks are   specified using the same notation.   <p>   <b>Note</b>: When DHCP is enabled, this property reflects the   current IP configuration and cannot be set.  When DHCP is not   enabled, this property can be set explicitly. |
| subnetMask | string | true | None | The subnet mask.   <p>   <b>Note</b>: When DHCP is not enabled, this property can be   set explicitly.  When DHCP is enabled, this property reflects the   current IP configuration and cannot be set. |
| ipV6Config | [vim.host.IpConfig.IpV6AddressConfiguration](vim.host.IpConfig.IpV6AddressConfiguration.md "vim.host.IpConfig.IpV6AddressConfiguration") | true | None | The ipv6 configuration |


