vim.net.IpConfigInfo
====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Protocol version independent address reporting data object for network   interfaces.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ipAddress | [vim.net.IpConfigInfo.IpAddress](vim.net.IpConfigInfo.IpAddress.md "vim.net.IpConfigInfo.IpAddress") | true | None | Zero, one or more manual (static) assigned IP addresses to be configured  on a given interface. |
| dhcp | [vim.net.DhcpConfigInfo](vim.net.DhcpConfigInfo.md "vim.net.DhcpConfigInfo") | true | None | Client side DHCP for a given interface. |
| autoConfigurationEnabled | bool | true | None | Enable or disable ICMPv6 router solictitation requests from a given interface  to acquire an IPv6 address and default gateway route from zero, one or more  routers on the connected network.   If not set then ICMPv6 is not available on this system,  See vim.host.Network.Capabilities |


