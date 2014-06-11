vim.net.DhcpConfigInfo.DhcpOptions
==================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Provides for reporting of DHCP client. This data object may be used  at a per interface or per system scope.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| enable | bool | None | None | Report state of dhcp client services. |
| config | [vim.KeyValue](vim.KeyValue.md "vim.KeyValue") | true | None | Platform specific settings for DHCP Client.  The key part is a unique number, the value part  is the platform specific configuration command.  For example on Linux, BSD systems using the file dhclient.conf  output would be reported at system scope:    key='1', value='timeout 60;'    key='2', value='reboot 10;'   output reported at per interface scope:    key='1', value='prepend domain-name-servers 192.0.2.1;'    key='2', value='equire subnet-mask, domain-name-servers;' |


