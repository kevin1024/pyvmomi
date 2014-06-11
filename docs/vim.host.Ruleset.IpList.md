vim.host.Ruleset.IpList
=======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ipAddress | string | true | None | The list of ipAddresses.   All IPv4 addresses are specified as strings using dotted   decimal format. For example, "192.0.20.10".   IPv6 addresses are 128-bit addresses represented   as eight fields of up to four hexadecimal digits. A colon separates each   field (:). For example, 2001:DB8:101::230:6eff:fe04:d9ff. The address can   also consist of  symbol '::' to represent multiple 16-bit groups of   contiguous 0's only once in an address as described in RFC 2373. |
| ipNetwork | [vim.host.Ruleset.IpNetwork](vim.host.Ruleset.IpNetwork.md "vim.host.Ruleset.IpNetwork") | true | None | The list of networks |
| allIp | bool | None | None | Flag indicating whether the ruleset works for all ip addresses. |


