vim.profile.DeferredPolicyOptionParameter
=========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.DeferredPolicyOptionParameter.md">ProfileDeferredPolicyOptionParameter</a> data object contains  information about a single deferred parameter for host configuration.  <p>  <ul>  <li>The Server verifies deferred parameter data when it calls the  <a href="vim.profile.host.HostProfile.md">HostProfile</a>.<a href="vim.profile.host.HostProfile.md#execute">ExecuteHostProfile</a>  method.<br/><br/></li>  <li>The client supplies deferred parameter data for host configuration when it calls the  <a href="vim.profile.host.ProfileManager.md">HostProfileManager</a>.<a href="vim.profile.host.ProfileManager.md#applyHostConfiguration">ApplyHostConfig_Task</a>  method.<br/><br/></li>  <li>The vCenter Server stores deferred parameter data in answer files  (<a href="vim.profile.host.AnswerFile.md">AnswerFile</a>.<a href="vim.profile.host.AnswerFile.md#userInput">userInput</a>).  <br/><br/></li>  </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| inputPath | [vim.profile.ProfilePropertyPath](vim.profile.ProfilePropertyPath.md "vim.profile.ProfilePropertyPath") | None | None | Complete path to the <a href="vim.profile.PolicyOption.md">PolicyOption</a> that defines the parameters. |
| parameter | [vmodl.KeyAnyValue](vmodl.KeyAnyValue.md "vmodl.KeyAnyValue") | true | None | List that contains values for the policy parameters.  <p>  During parameter verification, this property is unspecified  if the client has not provided the values for this parameter.  See <a href="vim.profile.host.ExecuteResult.md">ProfileExecuteResult</a>.<a href="vim.profile.host.ExecuteResult.md#requireInput">requireInput</a>. |


