vim.event.LockerReconfiguredEvent
=================================
inherits from [vim.event.Event](docs/vim.event.Event.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


Locker was reconfigured to a new location.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| oldDatastore | [vim.event.DatastoreEventArgument](vim.event.DatastoreEventArgument.md "vim.event.DatastoreEventArgument") | true | None | The datastore that was previously backing the locker. This field is not  set if a datastore was not backing the locker previously. |
| newDatastore | [vim.event.DatastoreEventArgument](vim.event.DatastoreEventArgument.md "vim.event.DatastoreEventArgument") | true | None | The datastore that is now used to back the locker.  This field is not set if no datastore is currently backing the locker. |


