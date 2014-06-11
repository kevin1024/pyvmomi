vim.event.VmBeingMigratedEvent
==============================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)


This event records that a virtual machine is being migrated.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| destHost | [vim.event.HostEventArgument](vim.event.HostEventArgument.md "vim.event.HostEventArgument") | None | None | The destination host. |
| destDatacenter | [vim.event.DatacenterEventArgument](vim.event.DatacenterEventArgument.md "vim.event.DatacenterEventArgument") | true | None | The destination datacenter |
| destDatastore | [vim.event.DatastoreEventArgument](vim.event.DatastoreEventArgument.md "vim.event.DatastoreEventArgument") | true | None | The destination primary datastore |


