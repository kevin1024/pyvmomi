vim.cluster.AttemptedVmInfo
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This data class reports virtual machine powerOn information.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vm | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | None | None | The virtual machine being powered on. |
| task | [vim.Task](vim.Task.md "vim.Task") | true | None | The ID of the task, which monitors powering on. |


