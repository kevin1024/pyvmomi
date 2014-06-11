vim.net.DhcpConfigInfo
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Dynamic Host Configuration Protocol reporting for IP version 4 and version 6.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ipv6 | [vim.net.DhcpConfigInfo.DhcpOptions](vim.net.DhcpConfigInfo.DhcpOptions.md "vim.net.DhcpConfigInfo.DhcpOptions") | true | None | IPv6 DHCP client settings. |
| ipv4 | [vim.net.DhcpConfigInfo.DhcpOptions](vim.net.DhcpConfigInfo.DhcpOptions.md "vim.net.DhcpConfigInfo.DhcpOptions") | true | None | IPv4 DHCP client settings. |


