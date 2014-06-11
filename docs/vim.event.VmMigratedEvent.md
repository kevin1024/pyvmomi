vim.event.VmMigratedEvent
=========================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)


This event records a virtual machine migration.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| sourceHost | [vim.event.HostEventArgument](vim.event.HostEventArgument.md "vim.event.HostEventArgument") | None | None | The source host.  (Because this is after a successful migration,   the destination host is recorded in the inherited "host" property.) |
| sourceDatacenter | [vim.event.DatacenterEventArgument](vim.event.DatacenterEventArgument.md "vim.event.DatacenterEventArgument") | true | None | The source datacenter |
| sourceDatastore | [vim.event.DatastoreEventArgument](vim.event.DatastoreEventArgument.md "vim.event.DatastoreEventArgument") | true | None | The source primary datastore |


