vim.host.NetStackInstance
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This class describes Network Stack Instance configuration

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | true | None | Key of instance    For instance which created by host, its value should be SystemStackKey. |
| name | string | true | None | The display name |
| dnsConfig | [vim.host.DnsConfig](vim.host.DnsConfig.md "vim.host.DnsConfig") | true | None | DNS configuration |
| ipRouteConfig | [vim.host.IpRouteConfig](vim.host.IpRouteConfig.md "vim.host.IpRouteConfig") | true | None | IP Route configuration |
| requestedMaxNumberOfConnections | int | true | None | The maximum number of socket connection that are requested on this instance |
| congestionControlAlgorithm | string | true | None | The TCP congest control algorithm used by this instance,    See CongestionControlAlgorithmType for valid values. |
| ipV6Enabled | bool | true | None | Enable or disable IPv6 protocol on this stack instance.  This property is not supported currently. |
| routeTableConfig | [vim.host.IpRouteTableConfig](vim.host.IpRouteTableConfig.md "vim.host.IpRouteTableConfig") | true | None |  |


