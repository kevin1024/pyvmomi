vim.host.FeatureMask
====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


A mask that is applied to a host feature capability.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Accessor name to the feature mask. |
| featureName | string | None | None | Name of the feature Identical to the key. |
| value | string | None | None | Opaque value to change the host feature capability to.   Masking operation is contained in the value. |


