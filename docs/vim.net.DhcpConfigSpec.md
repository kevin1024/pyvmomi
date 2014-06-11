vim.net.DhcpConfigSpec
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Dynamic Host Configuration Protocol Configuration for IP version 4 and version 6.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ipv6 | [vim.net.DhcpConfigSpec.DhcpOptionsSpec](vim.net.DhcpConfigSpec.DhcpOptionsSpec.md "vim.net.DhcpConfigSpec.DhcpOptionsSpec") | true | None | Configure IPv6 DHCP client settings. |
| ipv4 | [vim.net.DhcpConfigSpec.DhcpOptionsSpec](vim.net.DhcpConfigSpec.DhcpOptionsSpec.md "vim.net.DhcpConfigSpec.DhcpOptionsSpec") | true | None | Configure IPv4 DHCP client settings. |


