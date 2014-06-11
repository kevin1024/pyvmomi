vim.vm.device.VirtualPS2ControllerOption
========================================
inherits from [vim.vm.device.VirtualControllerOption](docs/vim.vm.device.VirtualControllerOption.md)


The VirtualPS2ControllerOption data object type contains the options    for a virtual PS/2 controller for keyboards and mice. In addition to    the options defined in the <a href="vim.vm.device.VirtualControllerOption.md">VirtualControllerOption</a> data object type, these options include the    number of keyboards and mice.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| numKeyboards | [vim.option.IntOption](vim.option.IntOption.md "vim.option.IntOption") | None | None | The minimum, maximum, and default number of keyboards you can   have at any given time. This is further constrained  by the number   of available slots in the PS/2 controller. The minimum, maximum,   and default are integers defined by three properties:   <p>   <ul>   <li><b>numKeyBoards.min</b>:  the minimum.   <li><b>numKeyBoards.max</b>:  the maximum.   <li><b>numKeyBoards.defaultValue</b>: the default number.   </ul> |
| numPointingDevices | [vim.option.IntOption](vim.option.IntOption.md "vim.option.IntOption") | None | None | The minimum, maximum, and default number of mice you can   have at any given time. The number of mice is also limited by the number   of available slots in the PS/2 controller. The minimum, maximum, and    default are integers defined by three properties:   <p>   <ul>   <li><b>numPointingDevices.min</b>: the minimum.   <li><b>numPointingDevices.max</b>: the maximum.   <li><b>numPointingDevices.defaultValue</b>: the default number.   </ul> |


