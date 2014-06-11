vim.event.VmMacConflictEvent
============================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)


This event records a MAC address conflict for a virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| conflictedVm | [vim.event.VmEventArgument](vim.event.VmEventArgument.md "vim.event.VmEventArgument") | None | None | The virtual machine whose MAC address conflicts with   the current virtual machine's address. |
| mac | string | None | None | The MAC address that is in conflict. |


