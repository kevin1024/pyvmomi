vim.profile.CompositeExpression
===============================
inherits from [vim.profile.Expression](docs/vim.profile.Expression.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


DataObject to Compose expressions. It is used to group expressions   together. They are similar to a parentheses in an expression.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| operator | string | None | None | Logical operator to be applied between the expressions in  the composite expression. e.g: or, and |
| expressionName | string | None | None | List of expression names that will be used for this composition.  The individual expressions will return a boolean. The return values   of the individual expressions will be used to compute the final  return value of the CompositeExpression.    The expressions specified in the list can themselves be   CompositeExpressions. |


