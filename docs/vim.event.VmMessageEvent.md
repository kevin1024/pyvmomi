vim.event.VmMessageEvent
========================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)


This event records when an informational message (consisting of a collection of "observations")  is thrown by the virtual machine. This is a generic event for such messages.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| message | string | None | None | A raw message returned by the virtualization platform. |
| messageInfo | [vim.vm.Message](vim.vm.Message.md "vim.vm.Message") | true | None |  |


