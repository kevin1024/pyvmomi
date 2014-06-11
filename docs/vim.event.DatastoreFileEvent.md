vim.event.DatastoreFileEvent
============================
inherits from [vim.event.DatastoreEvent](docs/vim.event.DatastoreEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Base class for events related to datastore file and directory  operations.  <p>  Property <I>datastore</I> inherited from DatastoreEvent refers  to the destination datastore in case there is more than datastore  involved in the operation.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| targetFile | string | None | None | Datastore path of the target file or directory. |


