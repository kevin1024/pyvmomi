vim.event.ExtendedEvent
=======================
inherits from [vim.event.GeneralEvent](docs/vim.event.GeneralEvent.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This event is the base class for extended events.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| eventTypeId | string | None | None | The id of the type of extended event. |
| managedObject | vim.ExtensibleManagedObject | None | None | The object on which the event was logged. |
| data | [vim.event.ExtendedEvent.Pair](vim.event.ExtendedEvent.Pair.md "vim.event.ExtendedEvent.Pair") | true | None | Key/value pairs associated with event. |


