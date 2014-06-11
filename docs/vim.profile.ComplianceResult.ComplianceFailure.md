vim.profile.ComplianceResult.ComplianceFailure
==============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| failureType | string | None | None | String uniquely identifying the failure. |
| message | [vmodl.LocalizableMessage](vmodl.LocalizableMessage.md "vmodl.LocalizableMessage") | None | None | Message which describes the compliance failures   message.key serves as a key to the localized  message catalog. |
| expressionName | string | true | None | Name of the Expression which generated the ComplianceFailure |


