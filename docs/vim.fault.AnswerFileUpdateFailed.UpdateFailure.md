vim.fault.AnswerFileUpdateFailed.UpdateFailure
==============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


DataObject which represents the errors that ocurred when an  answer file update was performed.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| userInputPath | [vim.profile.ProfilePropertyPath](vim.profile.ProfilePropertyPath.md "vim.profile.ProfilePropertyPath") | None | None | The user input that has the error |
| errMsg | [vmodl.LocalizableMessage](vmodl.LocalizableMessage.md "vmodl.LocalizableMessage") | None | None | Message which explains the error |


