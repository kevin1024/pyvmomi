vim.action.MethodAction
=======================
inherits from [vim.action.Action](docs/vim.action.Action.md)


This data object type defines an operation and its arguments, invoked   on a particular entity.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | Name of the operation. |
| argument | [vim.action.MethodActionArgument](vim.action.MethodActionArgument.md "vim.action.MethodActionArgument") | true | None | An array consisting of the arguments for the operation. |


