vim.profile.ExpressionMetadata
==============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


DataObject to represent the metadata associated with a SimpleExpression.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| expressionId | [vim.ExtendedElementDescription](vim.ExtendedElementDescription.md "vim.ExtendedElementDescription") | None | None | Id of the SimpleExpression |
| parameter | [vim.profile.ParameterMetadata](vim.profile.ParameterMetadata.md "vim.profile.ParameterMetadata") | true | None | Parameters that can be specified for this SimpleExpression |


