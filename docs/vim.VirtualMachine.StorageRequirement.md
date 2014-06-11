vim.VirtualMachine.StorageRequirement
=====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Describes the storage requirment to perform a consolidation  operation.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| datastore | [vim.Datastore](vim.Datastore.md "vim.Datastore") | None | None | The datastore. |
| freeSpaceRequiredInKb | long | None | None | Space required. |


