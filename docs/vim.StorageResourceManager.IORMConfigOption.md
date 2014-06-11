vim.StorageResourceManager.IORMConfigOption
===========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Configuration setting ranges for IORMConfigSpec object.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| enabledOption | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | None | None | enabledOption provides default state value for  <a href="vim.StorageResourceManager.IORMConfigSpec.md#enabled">enabled</a> |
| congestionThresholdOption | [vim.option.IntOption](vim.option.IntOption.md "vim.option.IntOption") | None | None | congestionThresholdOption defines value range which can be used for  <a href="vim.StorageResourceManager.IORMConfigSpec.md#congestionThreshold">congestionThreshold</a> |
| statsCollectionEnabledOption | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | None | None | statsCollectionEnabledOption provides default value for  <a href="vim.StorageResourceManager.IORMConfigSpec.md#statsCollectionEnabled">statsCollectionEnabled</a> |


