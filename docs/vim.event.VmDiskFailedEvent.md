vim.event.VmDiskFailedEvent
===========================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)


This event records a failure to create a virtual disk in a virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| disk | string | None | None | The name of the virtual disk. |
| reason | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | None | None | The reason for the failure. |


