vim.event.VmInstanceUuidConflictEvent
=====================================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This event records a conflict of virtual machine instance UUIDs.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| conflictedVm | [vim.event.VmEventArgument](vim.event.VmEventArgument.md "vim.event.VmEventArgument") | None | None | The virtual machine whose instance UUID conflicts with the   current virtual machine's instance UUID. |
| instanceUuid | string | None | None | The instance UUID in conflict. |


