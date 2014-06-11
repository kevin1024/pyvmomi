vim.host.IpRouteOp
==================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Routing Entry Operation.  Routing entries are individual static routes   which combined with the default route form all of the routing rules for   a host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| changeOperation | string | None | None | This property indicates the change operation to apply on    this configuration specification.<br>See <a href="vim.host.ConfigChange.Operation.md">HostConfigChangeOperation</a><br> |
| route | [vim.host.IpRouteEntry](vim.host.IpRouteEntry.md "vim.host.IpRouteEntry") | None | None | The routing entry itself |


