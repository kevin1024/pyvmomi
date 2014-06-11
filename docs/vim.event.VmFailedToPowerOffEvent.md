vim.event.VmFailedToPowerOffEvent
=================================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)


This event records a failure to power off a virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| reason | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | None | None | The reason for the failure. |


