vim.event.EventFilterSpec.ByEntity
==================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This option specifies a managed entity used to filter event history.     If the specified managed entity is a Folder or a ResourcePool, the query   will actually be performed on the entities contained within that Folder   or ResourcePool, so you cannot query for events on Folders and   ResourcePools themselves this way.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entity | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | None | System.View | The managed entity to which the event pertains. |
| recursion | [vim.event.EventFilterSpec.RecursionOption](vim.event.EventFilterSpec.RecursionOption.md "vim.event.EventFilterSpec.RecursionOption") | None | None | Specification of related managed entities in the inventory hierarchy. |


