vim.net.DhcpConfigSpec.DhcpOptionsSpec
======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Provides for configuration of IPv6

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| enable | bool | true | None | Enable or disable dhcp for IPv4. |
| config | [vim.KeyValue](vim.KeyValue.md "vim.KeyValue") | None | None | Platform specific settings for DHCP Client.  The key part is a unique number, the value part  is the platform specific configuration command.  See <a href="vim.net.DhcpConfigInfo.md">NetDhcpConfigInfo</a> for value formatting. |
| operation | string | None | None | Requires one of the values from <a href="vim.host.ConfigChange.Operation.md">HostConfigChangeOperation</a>. |


