vim.vm.AffinityInfo
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Specification of scheduling affinity.   <p>   Scheduling affinity is used for explicitly specifying which   processors or NUMA nodes may be used by a virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| affinitySet | int | true | None | List of nodes (processors for CPU, NUMA nodes for memory) that   may be used by the virtual machine.  If the array is empty when   modifying the affinity setting, then any existing affinity is removed. |


