vim.host.IpRouteConfigSpec
==========================
inherits from [vim.host.IpRouteConfig](docs/vim.host.IpRouteConfig.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Dataobject specifying the configuration for IpRoute

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| gatewayDeviceConnection | [vim.host.VirtualNicConnection](vim.host.VirtualNicConnection.md "vim.host.VirtualNicConnection") | true | None | Choose a gateway device based on what the VirtualNic is connected to.    This applies to service console gateway only, it      is ignored otherwise. |
| ipV6GatewayDeviceConnection | [vim.host.VirtualNicConnection](vim.host.VirtualNicConnection.md "vim.host.VirtualNicConnection") | true | None | The ipv6 gateway device based on what the VirtualNic is connected to.  This applies to service console gateway only, it     is ignored otherwise. |


