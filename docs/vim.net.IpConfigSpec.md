vim.net.IpConfigSpec
====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Internet Protocol Address Configuration for version 4 and version 6.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ipAddress | [vim.net.IpConfigSpec.IpAddressSpec](vim.net.IpConfigSpec.IpAddressSpec.md "vim.net.IpConfigSpec.IpAddressSpec") | true | None | A set of manual (static) IP addresses to be configured on a given interface. |
| dhcp | [vim.net.DhcpConfigSpec](vim.net.DhcpConfigSpec.md "vim.net.DhcpConfigSpec") | true | None | Configure client side DHCP for a given interface. |
| autoConfigurationEnabled | bool | true | None | Enable or disable ICMPv6 router solictitation requests from a given interface  to acquire an IPv6 address and default gateway route from zero, one or more  routers on the connected network. |


