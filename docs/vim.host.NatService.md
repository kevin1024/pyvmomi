vim.host.NatService
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


A network address translation (NAT) service instance provides    firewall and network address translation services for a virtual    network.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | The instance ID of the NAT service. |
| spec | [vim.host.NatService.Specification](vim.host.NatService.Specification.md "vim.host.NatService.Specification") | None | None | The configurable properties for the NatService object. |


