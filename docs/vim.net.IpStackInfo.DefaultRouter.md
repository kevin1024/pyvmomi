vim.net.IpStackInfo.DefaultRouter
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ipAddress | string | None | None | Unicast IP address of a next-hop router. |
| device | string | None | None | This value will contain the name of the interface as reported by the  operationg system. |
| lifetime | datetime | None | None | When this entry will no longer valid. For IPv6 this value  see For IPv6 RFC 2462 sections 4.2 and 6.3.4. |
| preference | string | None | None | Value of this entry compared to others that this IP stack uses  when making selection to route traffic on the default  route when there are multiple default routers. Value must be one of  <a href="vim.net.IpStackInfo.Preference.md">NetIpStackInfoPreference</a> |


