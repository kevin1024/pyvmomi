vim.host.IpRouteEntry
=====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


IpRouteEntry.  Routing entries are individual static routes which combined  with the default route form all of the routing rules for a host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| network | string | None | None | Network of the routing entry  Of the format "10.20.120.0" or "2001:db8::1428:57" |
| prefixLength | int | None | None | Prefix length of the network (this is the 22 in 10.20.120.0/22) |
| gateway | string | None | None | Gateway for the routing entry |
| deviceName | string | true | None | If available the property indicates the device associated with the  routing entry. This property can only be read from the server.  It will be ignored if set by the client. |


