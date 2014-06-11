vim.profile.ApplyProfileProperty
================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


The <a href="vim.profile.ApplyProfileProperty.md">ProfileApplyProfileProperty</a> data object defines one or more subprofiles.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| propertyName | string | None | None | Name of the property. |
| array | bool | None | None | Flag indicating whether this property is an array of profiles. |
| profile | [vim.profile.ApplyProfile](vim.profile.ApplyProfile.md "vim.profile.ApplyProfile") | true | None | Subprofiles that define policies and nested subprofiles. |


