vim.HbrManager.ReplicationVmInfo
================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


This data object represents the essential information about the  state of a given replicated <a href="vim.VirtualMachine.md">VirtualMachine</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| state | string | None | None | A string representing the current State of the virtual machine. |
| progressInfo | [vim.HbrManager.ReplicationVmInfo.ProgressInfo](vim.HbrManager.ReplicationVmInfo.ProgressInfo.md "vim.HbrManager.ReplicationVmInfo.ProgressInfo") | true | None | Progress stats for the current operation. Never present if the state is  not "syncing" or "active". If not present while in one of these states,  the host is still gathering initial operation statistics (progress can  be assumed to be 0). |
| imageId | string | true | None | An optional imageId that identifies the instance being created,  this is the imagId string that is passed to  <a href="vim.HbrManager.md#createInstance">HbrCreateInstance_Task</a> or  <a href="vim.HbrManager.md#startOfflineInstance">HbrStartOfflineInstance_Task</a> |
| lastError | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | A MethodFault representing the last replication specific error  that the <a href="vim.VirtualMachine.md">VirtualMachine</a> encountered during a create  instance operation. The successful creation of an instance  will clear any error. |


