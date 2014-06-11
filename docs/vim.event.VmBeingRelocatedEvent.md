vim.event.VmBeingRelocatedEvent
===============================
inherits from [vim.event.VmRelocateSpecEvent](docs/vim.event.VmRelocateSpecEvent.md)


This event records that a virtual machine is being relocated.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| destHost | [vim.event.HostEventArgument](vim.event.HostEventArgument.md "vim.event.HostEventArgument") | None | None | The destination host to which the virtual machine is being relocated. |
| destDatacenter | [vim.event.DatacenterEventArgument](vim.event.DatacenterEventArgument.md "vim.event.DatacenterEventArgument") | true | None | The destination datacenter to which the virtual machine is being relocated |
| destDatastore | [vim.event.DatastoreEventArgument](vim.event.DatastoreEventArgument.md "vim.event.DatastoreEventArgument") | true | None | The destination primary datastore to which the virtual machine is being relocated |


