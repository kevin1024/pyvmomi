vim.event.VmFailedToStandbyGuestEvent
=====================================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)


This event records a failure to set the guest on a virtual machine to a standby   state.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| reason | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | None | None | The reason for the failure. |


