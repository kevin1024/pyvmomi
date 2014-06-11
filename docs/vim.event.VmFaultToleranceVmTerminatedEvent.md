vim.event.VmFaultToleranceVmTerminatedEvent
===========================================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This event records a secondary or primary VM is terminated.   The reason could be : divergence, lost connection to secondary, partial   hardware failure of secondary, or by user.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| reason | string | true | None |  |


