vim.SessionManager.ServiceRequestSpec
=====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


This data object type describes a request to a service.   It is used as argument to   <a href="vim.SessionManager.md#acquireGenericServiceTicket">AcquireGenericServiceTicket</a>.    This is the base class for more specific service request specifications.   E.g. for HTTP services the derived class will provide a URL property.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


