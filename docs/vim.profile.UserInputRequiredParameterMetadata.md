vim.profile.UserInputRequiredParameterMetadata
==============================================
inherits from [vim.profile.PolicyOptionMetadata](docs/vim.profile.PolicyOptionMetadata.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.UserInputRequiredParameterMetadata.md">UserInputRequiredParameterMetadata</a> data object represents policy option metadata  information for configuration data. The Profile Engine saves configuration  data from the user input options in the host <a href="vim.profile.host.AnswerFile.md">AnswerFile</a>.  See the <a href="vim.profile.host.HostProfile.md#execute">ExecuteHostProfile</a> and  <a href="vim.profile.host.ProfileManager.md#applyHostConfiguration">ApplyHostConfig_Task</a> methods.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| userInputParameter | [vim.profile.ParameterMetadata](vim.profile.ParameterMetadata.md "vim.profile.ParameterMetadata") | true | None | Metadata for user input options. |


