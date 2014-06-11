vim.host.IpRouteTableConfig
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


IpRouteEntry.  Routing entries are individual static routes which combined   with the default route form all of the routing rules for a host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ipRoute | [vim.host.IpRouteOp](vim.host.IpRouteOp.md "vim.host.IpRouteOp") | true | None | The array of Routing ops (routes to be added/removed) |
| ipv6Route | [vim.host.IpRouteOp](vim.host.IpRouteOp.md "vim.host.IpRouteOp") | true | None |  |


