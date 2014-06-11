vim.VirtualApp.LinkInfo
=======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)
### DEPRECATED



Linked child information.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | None | None | The key contains a reference to the entity that is linked to this vApp |
| destroyWithParent | bool | true | None | Whether the entity should be removed, when this vApp is removed |


