vim.host.IpConfig.IpV6AddressConfiguration
==========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The ipv6 address configuration

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ipV6Address | [vim.host.IpConfig.IpV6Address](vim.host.IpConfig.IpV6Address.md "vim.host.IpConfig.IpV6Address") | true | None | Ipv6 adrresses configured on the interface. The global addresses can be configured  through DHCP, stateless or manual configuration. Link local addresses can be  only configured with the origin set to  <a href="vim.host.IpConfig.IpV6AddressConfigType.md#other">other</a>. |
| autoConfigurationEnabled | bool | true | None | Specify if IPv6 address and routing information information  be enabled or not as per RFC 2462. |
| dhcpV6Enabled | bool | true | None | The flag to indicate whether or not DHCP (dynamic host   control protocol) is enabled to obtain an ipV6 address.   If this property is set to true, an ipV6 address is configured through dhcpV6. |


