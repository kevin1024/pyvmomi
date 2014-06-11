vim.event.VmBeingHotMigratedEvent
=================================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)


This event records that a virtual machine is being hot-migrated.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| destHost | [vim.event.HostEventArgument](vim.event.HostEventArgument.md "vim.event.HostEventArgument") | None | None | The destination host to which the virtual machine is to be migrated. |
| destDatacenter | [vim.event.DatacenterEventArgument](vim.event.DatacenterEventArgument.md "vim.event.DatacenterEventArgument") | true | None | The destination datacenter to which the virtual machine is being migrated |
| destDatastore | [vim.event.DatastoreEventArgument](vim.event.DatastoreEventArgument.md "vim.event.DatastoreEventArgument") | true | None | The destination primary datastore to which the virtual machine is being migrated |


