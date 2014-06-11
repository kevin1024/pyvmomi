vim.event.VmRelocateFailedEvent
===============================
inherits from [vim.event.VmRelocateSpecEvent](docs/vim.event.VmRelocateSpecEvent.md)


This event records a failure to relocate a virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| destHost | [vim.event.HostEventArgument](vim.event.HostEventArgument.md "vim.event.HostEventArgument") | None | None | The destination host to which the virtual machine is being relocated. |
| reason | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | None | None | The reason why this relocate operation failed. |
| destDatacenter | [vim.event.DatacenterEventArgument](vim.event.DatacenterEventArgument.md "vim.event.DatacenterEventArgument") | true | None | The destination datacenter to which the virtual machine was being relocated |
| destDatastore | [vim.event.DatastoreEventArgument](vim.event.DatastoreEventArgument.md "vim.event.DatastoreEventArgument") | true | None | The destination primary datastore to which the virtual machine was being relocated |


