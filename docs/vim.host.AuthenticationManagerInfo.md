vim.host.AuthenticationManagerInfo
==================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


The <a href="vim.host.AuthenticationManagerInfo.md">HostAuthenticationManagerInfo</a> data object provides   access to authentication information for the ESX host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| authConfig | [vim.host.AuthenticationStoreInfo](vim.host.AuthenticationStoreInfo.md "vim.host.AuthenticationStoreInfo") | None | None | An array containing entries for local authentication and host  Active Directory authentication.   <ul>     <li><a href="vim.host.LocalAuthenticationInfo.md">HostLocalAuthenticationInfo</a> - Local authentication is always enabled.</li>     <li> <a href="vim.host.ActiveDirectoryInfo.md">HostActiveDirectoryInfo</a> - Host Active Directory authentication information         includes the name of the domain, membership status,         and a list of other domains trusted by the membership domain.     </li>   </ul> |


