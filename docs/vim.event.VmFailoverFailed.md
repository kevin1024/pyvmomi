vim.event.VmFailoverFailed
==========================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)


This event records when a virtual machine failover was unsuccessful.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| reason | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | The reason for the failure |


