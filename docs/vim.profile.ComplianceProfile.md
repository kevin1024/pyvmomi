vim.profile.ComplianceProfile
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


DataObject contains the verifications that need to be done  to make sure the entity is in compliance.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| expression | [vim.profile.Expression](vim.profile.Expression.md "vim.profile.Expression") | None | None | List of expressions that make up the ComplianceChecks. |
| rootExpression | string | None | None | Name of the Expression which is the root of the expression tree. |


