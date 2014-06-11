vim.event.VmAutoRenameEvent
===========================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)


This event records that a virtual machine was automatically renamed   because of a name conflict.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| oldName | string | None | None | The name of the virtual machine before renaming. |
| newName | string | None | None | The name of the virtual machine after renaming. |


