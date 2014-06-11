vim.fault.ConflictingConfiguration.Config
=========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This class defines the configuration that is in conflict.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entity | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | true | None | The entity on which the configuration is in conflict. |
| propertyPath | string | None | None | The property paths that are in conflict. |


