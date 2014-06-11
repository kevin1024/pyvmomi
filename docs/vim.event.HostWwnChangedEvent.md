vim.event.HostWwnChangedEvent
=============================
inherits from [vim.event.HostEvent](docs/vim.event.HostEvent.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This event records a change in a host's WWN (World Wide Name).

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| oldNodeWwns | long | true | None | The old node WWN. |
| oldPortWwns | long | true | None | The old port WWN. |
| newNodeWwns | long | true | None | The new node WWN. |
| newPortWwns | long | true | None | The new port WWN. |


