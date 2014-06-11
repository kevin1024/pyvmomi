vim.event.VmRelocatedEvent
==========================
inherits from [vim.event.VmRelocateSpecEvent](docs/vim.event.VmRelocateSpecEvent.md)


This event records the completion of a virtual machine relocation.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| sourceHost | [vim.event.HostEventArgument](vim.event.HostEventArgument.md "vim.event.HostEventArgument") | None | None | The source host from which the virtual machine was relocated. |
| sourceDatacenter | [vim.event.DatacenterEventArgument](vim.event.DatacenterEventArgument.md "vim.event.DatacenterEventArgument") | true | None | The source datacenter from which the virtual machine relocated |
| sourceDatastore | [vim.event.DatastoreEventArgument](vim.event.DatastoreEventArgument.md "vim.event.DatastoreEventArgument") | true | None | The source primary datastore from which the virtual machine relocated |


