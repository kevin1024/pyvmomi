vim.ServiceManager.ServiceInfo
==============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object represents essential information about a particular service.   The information is sufficient to be able to identify the service and retrieve   the object implementing it.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| serviceName | string | None | None | A service name. Each service is expected to create a unique name    for itself that can be used to locate the service. This name    does not need to be unique across hosts or other such locations though. |
| location | string | true | None | A list of data that can be used to uniquely identify a particular instance of a service.   Multiple instances of a service can exist across different domains (for instance, a service   that is associated with a particular virtual machine or a particular host). In such cases,   the service name is insufficient to identify the service and location data can be used   to identify the instance of interest. A service may publish as much location data   as is needed to identify it (e.g, vmware.host.<hostname> or vmware.vm.<uuid> or both).   The particular choice of locations have to be agreed upon by   the client and the service. |
| service | vim.ExtensibleManagedObject | None | None | The managed object that presents this service. |
| description | string | None | None | A description of the service. Provides help text on how   to use the service. |


