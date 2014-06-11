vim.event.VmFaultToleranceStateChangedEvent
===========================================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This event records a fault tolerance state change.   A default alarm will be triggered upon this event, which would   change the vm state:   the vm state is red if the newState is needSecondary;   the vm state is yellow if the newState is disabled;   the vm state is green if the newState is notConfigured, starting,   enabled or running

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| oldState | [vim.VirtualMachine.FaultToleranceState](vim.VirtualMachine.FaultToleranceState.md "vim.VirtualMachine.FaultToleranceState") | None | None | The old fault toleeance state. |
| newState | [vim.VirtualMachine.FaultToleranceState](vim.VirtualMachine.FaultToleranceState.md "vim.VirtualMachine.FaultToleranceState") | None | None | The new fault tolerance state. |


