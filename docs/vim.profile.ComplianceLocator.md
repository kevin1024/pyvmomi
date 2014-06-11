vim.profile.ComplianceLocator
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This dataObject contains information about location of applyProfile  which was responsible for generation of a particular ComplianceExpression.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| expressionName | string | None | None | Exression for which the Locator corresponds to |
| applyPath | [vim.profile.ProfilePropertyPath](vim.profile.ProfilePropertyPath.md "vim.profile.ProfilePropertyPath") | None | None | Complete path to the profile/policy which was responsible for the    generation of the ComplianceExpression.   [ProfilePath + policyId] will uniquely identify a Policy. |


