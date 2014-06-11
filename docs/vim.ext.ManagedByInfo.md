vim.ext.ManagedByInfo
=====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


The ManagedByInfo data object contains information about the extension   responsible for the life-cycle of the entity.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| extensionKey | string | None | None | Key of the extension managing the entity. |
| type | string | None | None | Managed entity type, as defined by the extension managing the entity.   An extension can manage different types of entities - different kinds   of virtual machines, vApps, etc. - and this property is used to find   the corresponding <a href="vim.ext.ManagedEntityInfo.md">managedEntityInfo</a>   entry from the extension. |


