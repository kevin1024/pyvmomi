vim.event.VmInstanceUuidChangedEvent
====================================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This event records a change in a virtual machine's instance UUID.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| oldInstanceUuid | string | None | None | The old instance UUID. |
| newInstanceUuid | string | None | None | The new instance UUID. |


