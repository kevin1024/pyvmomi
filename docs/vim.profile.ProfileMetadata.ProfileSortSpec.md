vim.profile.ProfileMetadata.ProfileSortSpec
===========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| policyId | string | None | None | The id of the policy used to sort instances of the profile |
| parameter | string | None | None | The parameter to be used for sorting. Note that if the policy to be  used for sorting has multiple possible policy options, all possible  policy options defined for that policy type must have this parameter. |


