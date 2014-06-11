vim.event.DatastoreCapacityIncreasedEvent
=========================================
inherits from [vim.event.DatastoreEvent](docs/vim.event.DatastoreEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This event records when increase in a datastore's capacity is observed.  It may happen due to different reasons, like extending or expanding a  datastore.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| oldCapacity | long | None | None | The old datastore capacity. |
| newCapacity | long | None | None | The new datastore capacity. |


