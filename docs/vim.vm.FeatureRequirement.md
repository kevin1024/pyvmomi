vim.vm.FeatureRequirement
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


Feature requirement contains a key, featureName and an opaque value

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Accessor name to the feature requirement test |
| featureName | string | None | None | Name of the feature. Identical to the key. |
| value | string | None | None | Opaque value for the feature operation. Operation is contained  in the value. |


