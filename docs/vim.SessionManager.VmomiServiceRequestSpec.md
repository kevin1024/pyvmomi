vim.SessionManager.VmomiServiceRequestSpec
==========================================
inherits from [vim.SessionManager.ServiceRequestSpec](docs/vim.SessionManager.ServiceRequestSpec.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


This data object type describes a request to invoke a specific method   in a VMOMI service.    It currenly only supports {link vim.SessionManager#cloneSession} method.   The GenericServiceTicket.id returned from   <a href="vim.SessionManager.md#acquireGenericServiceTicket">AcquireGenericServiceTicket</a> for this request   can be use for <a href="vim.SessionManager.md#cloneSession">CloneSession</a> to clone a session

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| method | string | None | None | Name of the method identified by this request spec |


