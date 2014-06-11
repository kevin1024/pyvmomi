vim.host.AuthenticationStoreInfo
================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


The <a href="vim.host.AuthenticationStoreInfo.md">HostAuthenticationStoreInfo</a> base class defines status information   for local and host Active Directory authentication.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| enabled | bool | None | None | Indicates whether the authentication store is configured.   <ul>     <li> Host Active Directory authentication - <code>enabled</code>          is <code>True</code> if the host is a member of a domain.     </li>     <li> Local authentication - <code>enabled</code> is always <code>True</code>.     </li>   </ul> |


