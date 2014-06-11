vim.event.VmMacAssignedEvent
============================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)


This event records the assignment of a new MAC address   to a virtual network adapter.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| adapter | string | None | None | The name of the virtual adapter. |
| mac | string | None | None | The new MAC address. |


