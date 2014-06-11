vim.profile.SimpleExpression
============================
inherits from [vim.profile.Expression](docs/vim.profile.Expression.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


DataObject represents a pre-defined expression

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| expressionType | string | None | None | Type of the simple expression to instantiate.  The expressionType should be derived from the available expressions as  listed in the metadata. |
| parameter | [vmodl.KeyAnyValue](vmodl.KeyAnyValue.md "vmodl.KeyAnyValue") | true | None | The parameters for the expressionType.  The list of parameters needed for a simple expression can   be obtained from the metadata. |


