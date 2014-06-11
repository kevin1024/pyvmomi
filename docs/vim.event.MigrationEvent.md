vim.event.MigrationEvent
========================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)


These are events used to describe migration warning and errors

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| fault | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | None | None | The fault that describes the migration issue. This is typically either a   MigrationFault or a VmConfigFault. |


