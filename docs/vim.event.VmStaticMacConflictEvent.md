vim.event.VmStaticMacConflictEvent
==================================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)


This event records a static MAC address conflict for a virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| conflictedVm | [vim.event.VmEventArgument](vim.event.VmEventArgument.md "vim.event.VmEventArgument") | None | None | The virtual machine whose static MAC address conflicts with   the current virtual machine's address. |
| mac | string | None | None | The static MAC address that is in conflict. |


