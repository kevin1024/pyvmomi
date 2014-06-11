vim.host.CacheConfigurationManager.CacheConfigurationSpec
=========================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Host cache configuration specification.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| datastore | [vim.Datastore](vim.Datastore.md "vim.Datastore") | None | None | Datastore used for swap performance enhancement. |
| swapSize | long | None | None | Space to allocate on this datastore to implement swap performance  enhancements, in MB.  This value should be less or equal to free space  capacity on the datastore <a href="vim.Datastore.Summary.md#freeSpace">freeSpace</a>. |


