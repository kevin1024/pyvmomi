vim.ServiceManager
==================
as of [VI API 2.5](vim.version.md#vim.version.version2)


The ServiceManager managed object is a singleton object that is used to present   services that are optional and not necessarily formally defined.      This directory makes available a list of such services and provides an easy way   to locate them. The service being represented can take arbitrary form here and    is thus represented by a generic ManagedObject. The expectation is that the    client side is knowledgeable of the instance type of the specific service it   is interested in using.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='service'>service</a> | [vim.ServiceManager.ServiceInfo](vim.ServiceManager.ServiceInfo.md "vim.ServiceManager.ServiceInfo") | true | Global.ServiceManagers | The full list of services available in this directory. |


QueryServiceList([serviceName](#string "string"), [location](#string "string"))
-------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | QueryServiceList |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | Global.ServiceManagers |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if both serviceName and location are not specified. |




