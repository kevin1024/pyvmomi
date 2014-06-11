vim.vm.VirtualHardware
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The VirtualHardware data object type contains the complete configuration   of the hardware in a virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| numCPU | int | None | None | Number of virtual CPUs present in this virtual machine. |
| numCoresPerSocket | int | true | None | Number of cores used to distribute virtual CPUs among sockets   in this virtual machine.   If the value is unset it implies to numCoresPerSocket = 1. |
| memoryMB | int | None | None | Memory size, in MB. |
| virtualICH7MPresent | bool | true | None | Does this virtual machine have Virtual Intel I/O Controller Hub 7 |
| virtualSMCPresent | bool | true | None | Does this virtual machine have System Management Controller |
| device | [vim.vm.device.VirtualDevice](vim.vm.device.VirtualDevice.md "vim.vm.device.VirtualDevice") | true | None | The set of virtual devices belonging to the virtual machine.   This list is unordered. |


