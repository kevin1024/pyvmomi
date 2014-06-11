vim.host.IscsiManager.IscsiStatus
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


The IscsiStatus data object describes the   status of an operation.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| reason | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | List of failure reason and associated remedy.    An array of fault codes associated with the failure. The fault itself   will provide an indication of the actual failure code and   <a href="vmodl.MethodFault.md#faultMessage">faultMessage</a> will indicate the remedy that   needs to be taken to correct the failure. |


