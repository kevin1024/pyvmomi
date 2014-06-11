vim.host.NatService.Specification
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This data object type provides the details about the   Network Address Translation (NAT) service.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| virtualSwitch | string | None | None | The name of the virtual switch to which nat service is connected. |
| activeFtp | bool | None | None | The flag to indicate whether or not non-passive mode FTP    connections should be allowed. |
| allowAnyOui | bool | None | None | The flag to indicate whether or not the NAT    Service allows media access control traffic from any    Organizational Unique Identifier (OUI)?     By default, it does not allow traffic that originated    from the host to avoid packet loops. |
| configPort | bool | None | None | The flag to indicate whether or not the NAT Service    should open a configuration port. |
| ipGatewayAddress | string | None | None | The IP address that the NAT Service should use on   the virtual network. |
| udpTimeout | int | None | None | The time allotted for UDP packets. |
| portForward | [vim.host.NatService.PortForwardSpecification](vim.host.NatService.PortForwardSpecification.md "vim.host.NatService.PortForwardSpecification") | true | None | The port forwarding specifications to allow network    connections to be initiated from outside the firewall. |
| nameService | [vim.host.NatService.NameServiceSpec](vim.host.NatService.NameServiceSpec.md "vim.host.NatService.NameServiceSpec") | true | None | The configuration of naming services.  These parameters are    specific to Windows. |


