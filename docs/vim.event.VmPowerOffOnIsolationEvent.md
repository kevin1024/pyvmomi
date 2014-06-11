vim.event.VmPowerOffOnIsolationEvent
====================================
inherits from [vim.event.VmPoweredOffEvent](docs/vim.event.VmPoweredOffEvent.md)


This event records when a virtual machine has been powered off on an isolated host   in a HA cluster.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| isolatedHost | [vim.event.HostEventArgument](vim.event.HostEventArgument.md "vim.event.HostEventArgument") | None | None | The isolated host on which a virtual machine is powered off. |


