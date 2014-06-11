vim.profile.ParameterMetadata
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.ParameterMetadata.md">ProfileParameterMetadata</a> data object represents the metadata information  for expressions, policy options, and host-specific configuration data.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | [vim.ExtendedElementDescription](vim.ExtendedElementDescription.md "vim.ExtendedElementDescription") | None | None | Identifier for the parameter. |
| type | string | None | None | Type of the parameter. |
| optional | bool | None | None | Whether the parameter is optional. |
| defaultValue | object | true | None | Default value that can be used for the parameter. |


