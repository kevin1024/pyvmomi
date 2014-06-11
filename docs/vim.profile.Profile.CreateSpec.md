vim.profile.Profile.CreateSpec
==============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Specification describing the parameters during Profile creation

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | true | None | Name of the profile |
| annotation | string | true | None | User Provided description of the profile |
| enabled | bool | true | None | Flag indicating if the Profile is enabled |


