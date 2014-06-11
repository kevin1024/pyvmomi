vim.host.DhcpService.Config
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This data object type describes the configuration of a DHCP service    instance representing both the configured properties   on the instance and identification information.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| changeOperation | string | true | None | Indicates the change operation to apply on this configuration   specification.<br>See <a href="vim.host.ConfigChange.Operation.md">HostConfigChangeOperation</a><br> |
| key | string | None | None | The instance ID of the DHCP service. |
| spec | [vim.host.DhcpService.Specification](vim.host.DhcpService.Specification.md "vim.host.DhcpService.Specification") | None | None | Specification of the DHCP service. |


