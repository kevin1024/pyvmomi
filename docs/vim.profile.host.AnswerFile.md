vim.profile.host.AnswerFile
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


The <a href="vim.profile.host.AnswerFile.md">AnswerFile</a> data object contains host-specific information that a host  will use in combination with a <a href="vim.profile.host.HostProfile.md">HostProfile</a> for configuration.  Answer files are stored on the vCenter Server, along with host profiles.  An answer file is always associated with a particular host.  <p>  To supply host-specific data:  <ul>  <li>Specify deferred parameters when you call the  <a href="vim.profile.host.HostProfile.md">HostProfile</a>.<a href="vim.profile.host.HostProfile.md#execute">ExecuteHostProfile</a>  method. The host profile engine will verify the set of parameters for the  additional configuration data.</li><br/>  <li>Use the complete required input list  (<a href="vim.profile.host.ExecuteResult.md">ProfileExecuteResult</a>.<a href="vim.profile.host.ExecuteResult.md#requireInput">requireInput</a>[])  as user input for the  <a href="vim.profile.host.ProfileManager.md">HostProfileManager</a>.<a href="vim.profile.host.ProfileManager.md#applyHostConfiguration">ApplyHostConfig_Task</a>  method. When you apply the profile, the vCenter Server saves the additional configuration  data in the <a href="vim.profile.host.AnswerFile.md#userInput">userInput</a> list.</li><br/>  <li>Use the <a href="vim.profile.host.ProfileManager.md">HostProfileManager</a>.<a href="vim.profile.host.ProfileManager.md#updateAnswerFile">UpdateAnswerFile_Task</a> method. This method will update an existing answer file or create a new one.</li>  </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| userInput | [vim.profile.DeferredPolicyOptionParameter](vim.profile.DeferredPolicyOptionParameter.md "vim.profile.DeferredPolicyOptionParameter") | true | None | List containing host-specific configuration data. |
| createdTime | datetime | None | None | Time at which the answer file was created. |
| modifiedTime | datetime | None | None | Time at which the answer file was last modified. |


