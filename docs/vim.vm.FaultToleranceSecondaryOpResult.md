vim.vm.FaultToleranceSecondaryOpResult
======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


FaultToleranceSecondaryOpResult is a data object that reports on   the outcome of the <a href="vim.VirtualMachine.md#createSecondary">CreateSecondaryVM_Task</a> or   <a href="vim.VirtualMachine.md#enableSecondary">EnableSecondaryVM_Task</a> operation.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vm | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | None | None | The Secondary VirtualMachine |
| powerOnAttempted | bool | None | None | Whether an attempt was made to power on the secondary. If   an attempt was made, <a href="vim.vm.FaultToleranceSecondaryOpResult.md#powerOnResult">powerOnResult</a> will report the   status of this attempt. |
| powerOnResult | [vim.cluster.PowerOnVmResult](vim.cluster.PowerOnVmResult.md "vim.cluster.PowerOnVmResult") | true | None | The powerOnResult property reports the outcome of powering on the   Secondary VirtualMachine if a power on was required. A power on will   be attempted if the Primary Virtual Machine is powered on when the    operation is performed. This object is only reported if <a href="vim.vm.FaultToleranceSecondaryOpResult.md#powerOnAttempted">powerOnAttempted</a> is true. If the outcome of the power-on attempt   is not successful, the returned <a href="vim.cluster.PowerOnVmResult.md">ClusterPowerOnVmResult</a>    object will include an instance of <a href="vim.cluster.NotAttemptedVmInfo.md">ClusterNotAttemptedVmInfo</a>   whereas if the attempt was successful, then an instance of    <a href="vim.cluster.AttemptedVmInfo.md">ClusterAttemptedVmInfo</a> is returned. When    <a href="vim.cluster.AttemptedVmInfo.md">ClusterAttemptedVmInfo</a> is returned, its    <a href="vim.cluster.AttemptedVmInfo.md#task">task</a> property is only set if the cluster   is a HA-only cluster. |


