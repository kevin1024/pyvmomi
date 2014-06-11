vim.UpdateVirtualMachineFilesResult
===================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


UpdateVirtualMachineFilesResult is the result returned   to the <a href="vim.Datastore.md#updateVirtualMachineFiles">UpdateVirtualMachineFiles_Task</a> method.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| failedVmFile | [vim.UpdateVirtualMachineFilesResult.FailedVmFileInfo](vim.UpdateVirtualMachineFilesResult.FailedVmFileInfo.md "vim.UpdateVirtualMachineFilesResult.FailedVmFileInfo") | true | None | The list of virtual machines files the server has attempted   to update but failed to update. |


