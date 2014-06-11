vim.event.VmResourcePoolMovedEvent
==================================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)


This event records when a virtual machine is moved from one resource pool to another.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| oldParent | [vim.event.ResourcePoolEventArgument](vim.event.ResourcePoolEventArgument.md "vim.event.ResourcePoolEventArgument") | None | None | The old parent resourcePool of the moved virtual machine. |
| newParent | [vim.event.ResourcePoolEventArgument](vim.event.ResourcePoolEventArgument.md "vim.event.ResourcePoolEventArgument") | None | None | The new parent resourcePool of the moved virtual machine. |


