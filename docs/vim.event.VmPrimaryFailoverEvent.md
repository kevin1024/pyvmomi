vim.event.VmPrimaryFailoverEvent
================================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This event records a fault tolerance failover.   The reason could be : lost connection to primary, partial hardware failure   of primary or by user.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| reason | string | true | None | The reason for the failure.  see <a href="vim.VirtualMachine.NeedSecondaryReason.md">VirtualMachineNeedSecondaryReason</a> |


