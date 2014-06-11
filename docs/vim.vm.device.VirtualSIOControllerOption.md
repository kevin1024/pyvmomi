vim.vm.device.VirtualSIOControllerOption
========================================
inherits from [vim.vm.device.VirtualControllerOption](docs/vim.vm.device.VirtualControllerOption.md)


The VirtualSIOControllerOption data object type contains the options    for a virtual Super IO Controller.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| numFloppyDrives | [vim.option.IntOption](vim.option.IntOption.md "vim.option.IntOption") | None | None | Three properties (numFloppyDrives.min, numFloppyDrives.max, and   numFloppyDrives.defaultValue) define the minimum, maximum, and default    number of floppy drives you can have at any given time in the Super IO    Controller. This is further constrained by the number of available    slots in the Super IO Controller. |
| numSerialPorts | [vim.option.IntOption](vim.option.IntOption.md "vim.option.IntOption") | None | None | Three properties (numSerialPorts.min, numSerialPorts.max, and   numSerialPorts.defaultValue) define the minimum, maximum, and default   number of serial ports you can   have at any given time in the Super IO Controller. This is further    constrained by the number of available slots in the Super IO    Controller. |
| numParallelPorts | [vim.option.IntOption](vim.option.IntOption.md "vim.option.IntOption") | None | None | Three properties (numParallelPorts.min, numParallelPorts.max, and   numParallelPorts.defaultValue) define the minimum, maximum, and default   number of parallel ports you can   have at any given time in the Super IO controller. This is further    constrained by the number of available slots in the Super IO    Controller. |


