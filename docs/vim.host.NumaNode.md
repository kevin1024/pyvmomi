vim.host.NumaNode
=================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Information about a single NUMA node.   <p>   NOTE: This data object is not modeled correctly if the NUMA node   contains multiple disjoint memory ranges. If there are multiple memory   ranges, the client will see one memory ranges from this NumaNode   object, and the memory range may or may not belong to this NUMA node.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| typeId | int | None | None | Zero-based NUMA ID for the node. |
| cpuID | short | None | None | Information about each of the CPUs associated with the node. |
| memoryRangeBegin | long | None | None | Beginning memory range for this NUMA node. |
| memoryRangeLength | long | None | None | Length of the memory range for this node in bytes, that is, the amount   of memory on the node. |


