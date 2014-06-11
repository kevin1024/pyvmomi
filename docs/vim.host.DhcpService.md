vim.host.DhcpService
====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


A dynamic host control protocol (DHCP) service instance serves IP    addresses to a single virtual network subnet.  The instances may    be handled collectively by a single server.  This decision can    be made during implementation.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | The instance ID of the DHCP service. |
| spec | [vim.host.DhcpService.Specification](vim.host.DhcpService.Specification.md "vim.host.DhcpService.Specification") | None | None | Configurable properties for the DHCP service. |


