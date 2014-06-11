vim.net.DnsConfigInfo
=====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Domain Name Server (DNS) Configuration Specification -   a data object for reporting the configuration of RFC 1034 client side DNS settings.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| dhcp | bool | None | None | Indicates whether or not dynamic host control   protocol (DHCP) is used to configure DNS configuration. |
| hostName | string | None | None | The host name portion of DNS name. For example, "esx01" part of   esx01.example.com. |
| domainName | string | None | None | The domain name portion of the DNS name.  "example.com" part of   esx01.example.com. |
| ipAddress | string | true | None | The IP addresses of the DNS servers in order of use.   IPv4 addresses are specified using   dotted decimal notation.  For example, "192.0.2.1".   IPv6 addresses are 128-bit addresses represented as   eight fields of up to four hexadecimal digits.   A colon separates each field (:). For example,   2001:DB8:101::230:6eff:fe04:d9ff. The address can also consist of the   symbol '::' to represent multiple 16-bit groups of   contiguous 0's only once in an address as described in RFC 2373. |
| searchDomain | string | true | None | The domain in which to search for hosts, placed in order of preference. |


