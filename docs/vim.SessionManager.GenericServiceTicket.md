vim.SessionManager.GenericServiceTicket
=======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


This data object represents a ticket which grants access to some service.  The ticket may be used only once and is valid only for the  <a href="vim.SessionManager.ServiceRequestSpec.md">SessionManagerServiceRequestSpec</a> with which it was acquired.    For HTTP service requests (when spec is of type HttpServiceRequestSpec)   the returned ticket must be used by setting   <a href="vim.SessionManager.GenericServiceTicket.md#id">id</a>   as the value of a special cookie in the HTTP request.   For CGI requests the name of this cookie is 'vmware_cgi_ticket'.    The use of the returned ticket for other services is to be defined.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | string | None | None | A unique string identifying the ticket. |
| hostName | string | true | None | The name of the host that the service is running on |
| sslThumbprint | string | true | None | The expected thumbprint of the SSL certificate of the host.   If it is empty, the host must be authenticated by name. |


