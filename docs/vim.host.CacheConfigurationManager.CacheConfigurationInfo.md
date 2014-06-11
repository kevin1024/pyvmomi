vim.host.CacheConfigurationManager.CacheConfigurationInfo
=========================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Host solid state drive cache configuration information.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | [vim.Datastore](vim.Datastore.md "vim.Datastore") | None | None | Datastore used for swap performance enhancements. |
| swapSize | long | None | None | Space allocated on this datastore to implement swap performance  enhancements, in MB. |


