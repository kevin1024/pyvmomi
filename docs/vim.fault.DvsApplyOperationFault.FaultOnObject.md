vim.fault.DvsApplyOperationFault.FaultOnObject
==============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


The fault occured during an apply operation.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| objectId | string | None | None | The object identifier. It should be UUID for vSphere Distributed Switches,    keys for vNetwork distributed portgroups and ports. |
| type | string | None | None | The Type of the objects. |
| fault | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | None | None | The fault that occured. |


