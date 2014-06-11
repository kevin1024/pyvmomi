vim.host.FeatureCapability
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


A feature that the host is able to provide at a particular value.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Accessor name to the feature capability. |
| featureName | string | None | None | Name of the feature. Identical to the key. |
| value | string | None | None | Opaque value that the feature is capable at. |


