vim.ResourcePlanningManager.InventoryDescription
================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Data object to capture all information needed to   describe a sample inventory.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| numHosts | int | None | None | The number of hosts. |
| numVirtualMachines | int | None | None | The number of virtual machines. |
| numResourcePools | int | true | None | The number of resource pools.  Default value is equal to numHosts |
| numClusters | int | true | None | The number of clusters.  Default value is equal to numHosts/5. |
| numCpuDev | int | true | None | The number cpu devices per host.  Default value is 4. |
| numNetDev | int | true | None | The number network devices per host.  Default value is 2. |
| numDiskDev | int | true | None | The number disk devices per host.  Default value is 10. |
| numvCpuDev | int | true | None | The number cpu devices per vm.  Default value is 2. |
| numvNetDev | int | true | None | The number network devices per vm.  Default value is 1. |
| numvDiskDev | int | true | None | The number disk devices per vm.  Default value is 4. |


