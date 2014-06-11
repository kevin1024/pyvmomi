vim.host.Summary.HardwareSummary
================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type summarizes hardware used by the host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vendor | string | None | None | The hardware vendor identification. |
| model | string | None | None | The system model identification. |
| uuid | string | None | None | The hardware BIOS identification. |
| otherIdentifyingInfo | [vim.host.SystemIdentificationInfo](vim.host.SystemIdentificationInfo.md "vim.host.SystemIdentificationInfo") | true | None | Other identification information. This information may be vendor   specific. |
| memorySize | long | None | None | The physical memory size in bytes. |
| cpuModel | string | None | None | The CPU model. |
| cpuMhz | int | None | None | The speed of the CPU cores. This is an average value if there are multiple   speeds. The product of cpuMhz and numCpuCores is approximately equal to the   sum of the MHz for all the individual cores on the host. |
| numCpuPkgs | short | None | None | Number of physical CPU packages on the host. Physical CPU packages are chips   that contain one or more processors. Processors contained by a package are   also known as CPU cores. For example, one dual-core package is comprised of   one chip that contains two CPU cores. |
| numCpuCores | short | None | None | Number of physical CPU cores on the host. Physical CPU cores are the   processors contained by a CPU package. |
| numCpuThreads | short | None | None | Number of physical CPU threads on the host. |
| numNics | int | None | None | The number of network adapters. |
| numHBAs | int | None | None | The number of host bus adapters (HBAs). |


