vim.event.LockerMisconfiguredEvent
==================================
inherits from [vim.event.Event](docs/vim.event.Event.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


Locker has not been configured properly.  This event is fired when the datastore configured to back the locker  does not exist or when connectivity to the datastore is lost.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| datastore | [vim.event.DatastoreEventArgument](vim.event.DatastoreEventArgument.md "vim.event.DatastoreEventArgument") | None | None | The datastore that has been configured to back the locker |


