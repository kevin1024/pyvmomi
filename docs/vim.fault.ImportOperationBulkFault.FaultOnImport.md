vim.fault.ImportOperationBulkFault.FaultOnImport
================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


The fault occurred on the entity during an import operation.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entityType | string | true | None | The entity type on which import failed. See <a href="vim.dvs.EntityBackup.EntityType.md">EntityType</a>   for valid values |
| key | string | true | None | The key on which import failed |
| fault | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | None | None | The fault that occurred. |


