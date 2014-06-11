vim.vm.device.VirtualIDEControllerOption
========================================
inherits from [vim.vm.device.VirtualControllerOption](docs/vim.vm.device.VirtualControllerOption.md)


The VirtualIDEControllerOption data object type contains the options   for a virtual IDE controller.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| numIDEDisks | [vim.option.IntOption](vim.option.IntOption.md "vim.option.IntOption") | None | None | The minimum, maximum, and default number of IDE VirtualDisk instances you can   have, at any given time, in the IDE controller. The number is further constrained   by the number of available slots in the virtual IDE controller. |
| numIDECdroms | [vim.option.IntOption](vim.option.IntOption.md "vim.option.IntOption") | None | None | The minimum, maximum, and default number of IDE VirtualCdrom instances you can   have, at any given time, in the IDE controller. The number is further constrained   by the number of available slots in the virtual IDE controller. |


