vim.host.Ruleset.IpNetwork
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| network | string | None | None | The IPv4 or IPv6 network.   All IPv4 subnet addresses are specified as strings using dotted   decimal format. For example, "192.0.20.0".   IPv6 addresses are 128-bit addresses represented   as eight fields of up to four hexadecimal digits. A colon separates each   field (:). For example, 2001:DB8:101::230:6eff:fe04:d9ff. The address can   also consist of  symbol '::' to represent multiple 16-bit groups of   contiguous 0's only once in an address as described in RFC 2373. |
| prefixLength | int | None | None | The prefix length for the network.   For example the prefix length for a network 10.20.120/22 is 22 |


