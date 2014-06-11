vim.cluster.PowerOnVmResult
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


PowerOnVmResult is the base class of the result returned to the    <a href="vim.Datacenter.md#powerOnVm">PowerOnMultiVM_Task</a> method.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| attempted | [vim.cluster.AttemptedVmInfo](vim.cluster.AttemptedVmInfo.md "vim.cluster.AttemptedVmInfo") | true | None | The list of virtual machines the Virtual Center has attempted to power on.  For a virtual machine not managed by DRS, a task ID is also returned. |
| notAttempted | [vim.cluster.NotAttemptedVmInfo](vim.cluster.NotAttemptedVmInfo.md "vim.cluster.NotAttemptedVmInfo") | true | None | The list of virtual machines DRS can not find suitable hosts for powering on.  There is one fault associated with each virtual machine. |
| recommendations | [vim.cluster.Recommendation](vim.cluster.Recommendation.md "vim.cluster.Recommendation") | true | None | The list of recommendations that need the client to approve manually. |


