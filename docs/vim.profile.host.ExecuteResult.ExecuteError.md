vim.profile.host.ExecuteResult.ExecuteError
===========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.host.ExecuteResult.ExecuteError.md">ProfileExecuteError</a> data object  describes an error encountered during host profile execution.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| path | [vim.profile.ProfilePropertyPath](vim.profile.ProfilePropertyPath.md "vim.profile.ProfilePropertyPath") | true | None | Path to the profile or policy with which the error is associated. |
| message | [vmodl.LocalizableMessage](vmodl.LocalizableMessage.md "vmodl.LocalizableMessage") | None | None | Message describing the error. |


