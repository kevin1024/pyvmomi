vim.host.ActiveDirectoryInfo
============================
inherits from [vim.host.DirectoryStoreInfo](docs/vim.host.DirectoryStoreInfo.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


The <a href="vim.host.ActiveDirectoryInfo.md">HostActiveDirectoryInfo</a> data object describes ESX host   membership in an Active Directory domain. If the   <a href="vim.host.AuthenticationStoreInfo.md">HostAuthenticationStoreInfo</a>.<a href="vim.host.AuthenticationStoreInfo.md#enabled">enabled</a>   property is <code>True</code>, the host is a member of a domain   and the ESX Server will set the domain information properties.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| joinedDomain | string | true | None | The domain that this host joined. |
| trustedDomain | string | true | None | List of domains with which the <code>joinedDomain</code> has a trust.   The <code>joinedDomain</code> is not included in the   <code>trustedDomain</code> list. |
| domainMembershipStatus | string | true | None | Health information about the domain membership.   See <a href="vim.host.ActiveDirectoryInfo.DomainMembershipStatus.md">HostActiveDirectoryInfoDomainMembershipStatus</a>. |


