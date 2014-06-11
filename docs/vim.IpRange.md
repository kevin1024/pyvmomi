vim.IpRange
===========
inherits from [vim.IpAddress](docs/vim.IpAddress.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This class specifies a range of IP addresses by using prefix.   Usage: 128.20.20.10/24. Here 128.20.20.10 is IP address   and 24 is prefix length.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| addressPrefix | string | None | None | IP address prefix. |
| prefixLength | int | true | None | Prefix length with max value of 32 for IPv4 and 128 for IPv6. |


