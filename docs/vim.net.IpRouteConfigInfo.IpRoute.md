vim.net.IpRouteConfigInfo.IpRoute
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


IpRoute report an individual host, network or default destination network  reachable through a given gateway.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| network | string | None | None | IP Address of the destination IP network.  IPv6 addresses are 128-bit addresses represented  as eight fields of up to four hexadecimal digits. A colon separates each  field (:). For example, 2001:DB8:101::230:6eff:fe04:d9ff. The address can  also consist of  symbol '::' to represent multiple 16-bit groups of  contiguous 0's only once in an address as described in RFC 2373. |
| prefixLength | int | None | None | The prefix length. For IPv4 the value range is 0-31.  For IPv6 prefixLength is a decimal value range 0-127. The property  represents the number of contiguous, higher-order bits of the address that make  up the network portion of the IP address. |
| gateway | [vim.net.IpRouteConfigInfo.Gateway](vim.net.IpRouteConfigInfo.Gateway.md "vim.net.IpRouteConfigInfo.Gateway") | None | None | Where to send the packets for this route. |


