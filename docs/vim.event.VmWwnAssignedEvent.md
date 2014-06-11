vim.event.VmWwnAssignedEvent
============================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This event records the assignment of a new WWN (World Wide Name)   to a virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| nodeWwns | long | None | None | The new node WWN. |
| portWwns | long | None | None | The new port WWN. |


