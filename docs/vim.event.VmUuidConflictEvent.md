vim.event.VmUuidConflictEvent
=============================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)


This event records a conflict of virtual machine BIOS UUIDs.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| conflictedVm | [vim.event.VmEventArgument](vim.event.VmEventArgument.md "vim.event.VmEventArgument") | None | None | The virtual machine whose UUID conflicts with the   current virtual machine's UUID. |
| uuid | string | None | None | The BIOS UUID in conflict. |


