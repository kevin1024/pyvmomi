vim.host.HardwareInfo
=====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The HardwareInfo data object type describes the hardware   configuration of the host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| systemInfo | [vim.host.SystemInfo](vim.host.SystemInfo.md "vim.host.SystemInfo") | None | None | Information about the system as a whole. |
| cpuPowerManagementInfo | [vim.host.CpuPowerManagementInfo](vim.host.CpuPowerManagementInfo.md "vim.host.CpuPowerManagementInfo") | true | None |  |
| cpuInfo | [vim.host.CpuInfo](vim.host.CpuInfo.md "vim.host.CpuInfo") | None | None | Overall CPU information. |
| cpuPkg | [vim.host.CpuPackage](vim.host.CpuPackage.md "vim.host.CpuPackage") | None | None | Information about each of the physical CPU packages on the host. |
| memorySize | long | None | None | Total amount of physical memory on the host in bytes. |
| numaInfo | [vim.host.NumaInfo](vim.host.NumaInfo.md "vim.host.NumaInfo") | true | None | Information about the NUMA (non-uniform memory access). |
| smcPresent | bool | None | None | Presence of System Management Controller, indicates the host is  Apple hardware, and thus capable of running Mac OS guest as VM. |
| pciDevice | [vim.host.PciDevice](vim.host.PciDevice.md "vim.host.PciDevice") | true | None | The list of Peripheral Component Interconnect (PCI) devices   available on this host. |
| cpuFeature | [vim.host.CpuIdInfo](vim.host.CpuIdInfo.md "vim.host.CpuIdInfo") | true | None | CPU feature set that is supported by the hardware. This is the   intersection of the feature sets supported by the individual CPU   packages. This feature set is modified by the   <a href="vim.host.Capability.md#supportedCpuFeature">supportedCpuFeature</a>   array in the host capabilities to obtain the feature set supported by   the virtualization platform. |
| biosInfo | [vim.host.BIOSInfo](vim.host.BIOSInfo.md "vim.host.BIOSInfo") | true | None | Information about the system BIOS |
| reliableMemoryInfo | [vim.host.ReliableMemoryInfo](vim.host.ReliableMemoryInfo.md "vim.host.ReliableMemoryInfo") | true | None | Information about reliable memory. |


