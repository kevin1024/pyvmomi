vim.event.DatastoreFileCopiedEvent
==================================
inherits from [vim.event.DatastoreFileEvent](docs/vim.event.DatastoreFileEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This event records copy of a file or directory.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| sourceDatastore | [vim.event.DatastoreEventArgument](vim.event.DatastoreEventArgument.md "vim.event.DatastoreEventArgument") | None | None | Source datastore. |
| sourceFile | string | None | None | Datastore path of the source file or directory. |


