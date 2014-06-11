vim.event.VmBeingClonedNoFolderEvent
====================================
inherits from [vim.event.VmCloneEvent](docs/vim.event.VmCloneEvent.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


This event records a virtual machine being cloned.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| destName | string | None | None | The name of the destination virtual machine. |
| destHost | [vim.event.HostEventArgument](vim.event.HostEventArgument.md "vim.event.HostEventArgument") | None | None | The destination host to which the virtual machine is being cloned. |


