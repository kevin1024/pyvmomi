vim.TaskFilterSpec.ByEntity
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type specifies a managed entity used to    filter task history.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entity | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | None | System.View | The managed entity to which the task pertains. |
| recursion | [vim.TaskFilterSpec.RecursionOption](vim.TaskFilterSpec.RecursionOption.md "vim.TaskFilterSpec.RecursionOption") | None | None | Specification of related managed entities in the inventory hierarchy. |


