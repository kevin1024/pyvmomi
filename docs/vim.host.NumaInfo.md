vim.host.NumaInfo
=================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Information about NUMA (non-uniform memory access).

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| type | string | None | None | The type of NUMA technology. |
| numNodes | int | None | None | The number of NUMA nodes on the host. The value is 0 if the   host is not NUMA-capable. |
| numaNode | [vim.host.NumaNode](vim.host.NumaNode.md "vim.host.NumaNode") | true | None | Information about each of the NUMA nodes on the host.   The array is empty if the host is not NUMA-capable. |


