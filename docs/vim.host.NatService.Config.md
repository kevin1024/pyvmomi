vim.host.NatService.Config
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This data object type describes the network address    translation (NAT) service configuration    representing both the configured properties   on a NAT Service and identification information.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| changeOperation | string | true | None | Indicates the change operation to apply on this configuration   specification.<br>See <a href="vim.host.ConfigChange.Operation.md">HostConfigChangeOperation</a><br> |
| key | string | None | None | The instance ID of the NAT service. |
| spec | [vim.host.NatService.Specification](vim.host.NatService.Specification.md "vim.host.NatService.Specification") | None | None | The specification of the NAT service. |


