vim.SessionManager.HttpServiceRequestSpec
=========================================
inherits from [vim.SessionManager.ServiceRequestSpec](docs/vim.SessionManager.ServiceRequestSpec.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


This data object type describes a request to an HTTP or HTTPS service.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| method | string | true | None | The HTTP method used for the request.   If null, then any method is assumed.   <p><br>See <a href="vim.SessionManager.HttpServiceRequestSpec.Method.md">SessionManagerHttpServiceRequestSpecMethod</a><br> |
| url | string | None | None | URL of the HTTP request.   E.g. 'https://127.0.0.1:8080/cgi-bin/vm-support.cgi?n=val'.   <p>   For ESXi CGI service requests:   <li> only the path and query parts of the URL are used        (e.g. "/cgi-bin/vm-support.cgi?n=val"). </li>   This is so because the scheme is not known to the CGI service,   and the port may not be the same if using a proxy.   <p> |


