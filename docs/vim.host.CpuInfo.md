vim.host.CpuInfo
================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Information about the CPUs.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| numCpuPackages | short | None | None | Number of physical CPU packages on the host. |
| numCpuCores | short | None | None | Number of physical CPU cores on the host. |
| numCpuThreads | short | None | None | Number of physical CPU threads on the host. |
| hz | long | None | None | CPU speed per core. This might be an averaged value if the speed   is not uniform across all cores. The total CPU speed of the box is   defined as hz * numCpuCores |


