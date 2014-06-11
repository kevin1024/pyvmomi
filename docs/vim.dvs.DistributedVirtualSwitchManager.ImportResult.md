vim.dvs.DistributedVirtualSwitchManager.ImportResult
====================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


The <a href="vim.dvs.DistributedVirtualSwitchManager.ImportResult.md">DistributedVirtualSwitchManagerImportResult</a>  data object represents the results of a  <a href="vim.dvs.DistributedVirtualSwitchManager.md#importEntity">DVSManagerImportEntity_Task</a>  operation. It contains lists of the switches and portgroups  that were created. It also contains a list of faults  that occurred during the operation.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| distributedVirtualSwitch | [vim.DistributedVirtualSwitch](vim.DistributedVirtualSwitch.md "vim.DistributedVirtualSwitch") | true | None | List of distributed virtual switches. |
| distributedVirtualPortgroup | [vim.dvs.DistributedVirtualPortgroup](vim.dvs.DistributedVirtualPortgroup.md "vim.dvs.DistributedVirtualPortgroup") | true | None | List of distributed virtual portgroups. |
| importFault | [vim.fault.ImportOperationBulkFault.FaultOnImport](vim.fault.ImportOperationBulkFault.FaultOnImport.md "vim.fault.ImportOperationBulkFault.FaultOnImport") | true | None | Faults that occurred on the entities during the import operation. |


