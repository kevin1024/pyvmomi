vim.host.AuthenticationStore
============================
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


The <a href="vim.host.AuthenticationStore.md">HostAuthenticationStore</a> base class represents both local user   and host Active Directory authentication for an ESX host.   <ul>     <li>Local user authentication is always enabled. The vSphere API         does not support local user configuration for a host.     <li>Active Directory authentication for ESX hosts relies on         an established Active Directory account that         has the authority to add the host to a domain.   </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='info'>info</a> | [vim.host.AuthenticationStoreInfo](vim.host.AuthenticationStoreInfo.md "vim.host.AuthenticationStoreInfo") | None | None | Information about the authentication store. |


