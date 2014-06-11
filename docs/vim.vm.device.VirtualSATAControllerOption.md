vim.vm.device.VirtualSATAControllerOption
=========================================
inherits from [vim.vm.device.VirtualControllerOption](docs/vim.vm.device.VirtualControllerOption.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


The VirtualSATAControllerOption data object type contains the options   for a virtual SATA controller defined by the   <a href="vim.vm.device.VirtualSATAController.md">VirtualSATAController</a>   data object type.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| numSATADisks | [vim.option.IntOption](vim.option.IntOption.md "vim.option.IntOption") | None | None | Three properties (numSATADisks.min, numSATADisks.max, and   numSATADisks.defaultValue) define the minimum, maximum, and default   number of SATA VirtualDisk instances available at any given time in the   SATA controller. The number of SATA VirtualDisk instances is   also limited by the number of available slots in the SATA controller. |
| numSATACdroms | [vim.option.IntOption](vim.option.IntOption.md "vim.option.IntOption") | None | None | Three properties (numSATACdroms.min, numSATACdroms.max, and   numSATACdroms.defaultValue) define the minimum, maximum, and default   number of SATA VirtualCdrom instances available   in the SATA controller. The number of SATA VirtualCdrom instances is   also limited by the number of available slots in the SATA controller. |


