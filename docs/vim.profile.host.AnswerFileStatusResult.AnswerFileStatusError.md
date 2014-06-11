vim.profile.host.AnswerFileStatusResult.AnswerFileStatusError
=============================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


The AnswerFileStatusError data object describes an answer file  error and identifies the profile or policy option with which the error  is associated.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| userInputPath | [vim.profile.ProfilePropertyPath](vim.profile.ProfilePropertyPath.md "vim.profile.ProfilePropertyPath") | None | None | Path to a profile or a policy option for host-specific data. |
| errMsg | [vmodl.LocalizableMessage](vmodl.LocalizableMessage.md "vmodl.LocalizableMessage") | None | None | Message describing the error. |


