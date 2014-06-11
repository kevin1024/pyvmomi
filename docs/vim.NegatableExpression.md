vim.NegatableExpression
=======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


The base class for any type of setting or configuration to which negation   can be applied.   When used in a configuration information object:   if <a href="vim.NegatableExpression.md#negate">negate</a> is true, then ~(objectValue) will be used for the   configuration. If false, then objectValue will be used as it is.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| negate | bool | true | None | Whether the configuration needs to be negated or not. |


