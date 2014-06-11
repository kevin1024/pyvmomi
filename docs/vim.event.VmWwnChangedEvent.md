vim.event.VmWwnChangedEvent
===========================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This event records a change in a virtual machine's WWN (World Wide Name).

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| oldNodeWwns | long | true | None | The old node WWN. |
| oldPortWwns | long | true | None | The old port WWN. |
| newNodeWwns | long | true | None | The new node WWN. |
| newPortWwns | long | true | None | The new port WWN. |


