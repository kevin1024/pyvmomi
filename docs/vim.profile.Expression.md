vim.profile.Expression
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | string | None | None | Identifier of this expression. The id has to be unique within a Profile.  The id can be used as a key while building composite expressions. |
| displayName | string | None | None | User visible display name |
| negated | bool | None | None | Flag indicating if the condition of the expression should be negated.  e.g: conditions like VSwitch0 has vmnic0 connected to it can be turned into   VSwitch0 doesn't have vmnic0 connected to it. |


