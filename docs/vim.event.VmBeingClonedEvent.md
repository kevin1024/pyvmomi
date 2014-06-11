vim.event.VmBeingClonedEvent
============================
inherits from [vim.event.VmCloneEvent](docs/vim.event.VmCloneEvent.md)


This event records a virtual machine being cloned.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| destFolder | [vim.event.FolderEventArgument](vim.event.FolderEventArgument.md "vim.event.FolderEventArgument") | None | None | The destination folder to which the virtual machine is being cloned. |
| destName | string | None | None | The name of the destination virtual machine. |
| destHost | [vim.event.HostEventArgument](vim.event.HostEventArgument.md "vim.event.HostEventArgument") | None | None | The destination host to which the virtual machine is being cloned. |


