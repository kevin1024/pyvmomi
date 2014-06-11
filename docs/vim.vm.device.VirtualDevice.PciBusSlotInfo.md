vim.vm.device.VirtualDevice.PciBusSlotInfo
==========================================
inherits from [vim.vm.device.VirtualDevice.BusSlotInfo](docs/vim.vm.device.VirtualDevice.BusSlotInfo.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


The <code><a href="vim.vm.device.VirtualDevice.PciBusSlotInfo.md">VirtualDevicePciBusSlotInfo</a></code> data object type   defines information about a pci bus slot of pci device in a virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| pciSlotNumber | int | None | None | The pci slot number of the virtual device.   <p>   The pci slot number assignment should generally be left to the system.   If assigned  a value, and the value is invalid or duplicated, it will   automatically be reassigned. This will not cause an error.   <p>   Generally, the PCI slot numbers should never be specified in an   Reconfigure operation, and only in a CreateVM operation if i) they   are specified for all devices, and ii) the  numbers have been   determined by looking at an existing VM configuration of similar   hardware version. In other words, when the virtual hardware configuration   is duplicated. |


