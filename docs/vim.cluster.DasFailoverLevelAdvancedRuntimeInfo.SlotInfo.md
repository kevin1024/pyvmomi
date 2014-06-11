vim.cluster.DasFailoverLevelAdvancedRuntimeInfo.SlotInfo
========================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


A slot represents an amount of memory and cpu resources on a physical host for use  by a virtual machine. It is used in computing the resources to be reserved for  failover.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| numVcpus | int | None | None | The number of virtual cpus of a slot is defined as the maximum number of  virtual cpus any powered on virtual machine has. |
| cpuMHz | int | None | None | The cpu speed of a slot is defined as the maximum cpu reservation of any  powered on virtual machine in the cluster, or any otherwise defined minimum,  whichever is larger. |
| memoryMB | int | None | None | The memory size of a slot is defined as the maximum memory reservation plus  memory overhead of any powered on virtual machine in the cluster, or any  otherwise defined minimum, whichever is larger. |


