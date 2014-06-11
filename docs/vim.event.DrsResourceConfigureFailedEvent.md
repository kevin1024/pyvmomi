vim.event.DrsResourceConfigureFailedEvent
=========================================
inherits from [vim.event.HostEvent](docs/vim.event.HostEvent.md)


This event records when resource configuration   specification synchronization fails on a host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| reason | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | None | None | The reason for the failure. |


