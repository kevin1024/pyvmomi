vim.net.IpStackInfo
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Protocol version independent reporting data object for IP stack.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| neighbor | [vim.net.IpStackInfo.NetToMedia](vim.net.IpStackInfo.NetToMedia.md "vim.net.IpStackInfo.NetToMedia") | true | None | Zero, one or more entries of neighbors discovered using ARP or NDP.  This information is used to help diagnose connectivity or performance  issues. This property maps to RFC 4293 ipNetToPhysicalTable. |
| defaultRouter | [vim.net.IpStackInfo.DefaultRouter](vim.net.IpStackInfo.DefaultRouter.md "vim.net.IpStackInfo.DefaultRouter") | true | None | Zero one or more entries of discovered IP routers that are directly  reachable from a an interface on this system.  This property maps to RFC 4293 ipDefaultRouterTable. |


