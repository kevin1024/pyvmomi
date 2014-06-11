vim.profile.host.AnswerFileStatusResult
=======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


The <a href="vim.profile.host.AnswerFileStatusResult.md">AnswerFileStatusResult</a> data object shows the validity of the  answer file associated with a host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| checkedTime | datetime | None | None | Time that the answer file status was determined. |
| host | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | None | None | Host associated with the answer file. |
| status | string | None | None | Status of the answer file.  See <a href="vim.profile.host.ProfileManager.AnswerFileStatus.md">HostProfileManagerAnswerFileStatus</a> for valid values. |
| error | [vim.profile.host.AnswerFileStatusResult.AnswerFileStatusError](vim.profile.host.AnswerFileStatusResult.AnswerFileStatusError.md "vim.profile.host.AnswerFileStatusResult.AnswerFileStatusError") | true | None | If <code>status</code> is <code>invalid</code>, this property contains a list  of status error objects. |


