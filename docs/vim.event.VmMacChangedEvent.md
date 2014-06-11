vim.event.VmMacChangedEvent
===========================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)


This event records a change in a virtual machine's MAC address.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| adapter | string | None | None | The name of the virtual network adapter. |
| oldMac | string | None | None | The old MAC address. |
| newMac | string | None | None | The new MAC address. |


