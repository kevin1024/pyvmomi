vim.host.DnsConfig
==================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes the DNS configuration.   <p>   All IPv4 addresses, subnet addresses, and netmasks are specified using    dotted decimal notation.  For example, "192.0.2.1".    IPv6 addresses are 128-bit addresses represented as    eight fields of up to four hexadecimal digits.    A colon separates each field (:). For example,    2001:DB8:101::230:6eff:fe04:d9ff. The address can also consist of the    symbol '::' to represent multiple 16-bit groups of   contiguous 0's only once in an address as described in RFC 2373.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| dhcp | bool | None | None | The flag to indicate whether or not DHCP (dynamic host control    protocol) is used to determine DNS configuration automatically. |
| virtualNicDevice | string | true | None | If DHCP is enabled, the DHCP DNS of the service console network   adapter will override the system DNS. This field is ignored    if DHCP is disabled by the <a href="vim.host.DnsConfig.md#dhcp">dhcp</a> property. |
| hostName | string | None | None | The host name portion of DNS name.  For example, "esx01".   <p>   <b>Note</b>:  When DHCP is not enabled, the property can be set    explicitly.  When DHCP is enabled, the property reflects the current    DNS configuration, but cannot be set. |
| domainName | string | None | None | The domain name portion of the DNS name.  For example, "vmware.com".   <p>   <b>Note</b>:  When DHCP is not enabled, the property can be set    explicitly.  When DHCP is enabled, the property reflects the current    DNS configuration, but cannot be set. |
| address | string | true | None | The IP addresses of the DNS servers, placed in order of preference.   <p>   <b>Note</b>:  When DHCP is not enabled, the property can be set    explicitly.  When DHCP is enabled, the property reflects the current    DNS configuration, but cannot be set. |
| searchDomain | string | true | None | The domain in which to search for hosts, placed in order of preference.   <p>   <b>Note</b>:  When DHCP is not enabled, the property can be set    explicitly.  When DHCP is enabled, the property reflects the current    DNS configuration, but cannot be set. |


