vim.event.VmShutdownOnIsolationEvent
====================================
inherits from [vim.event.VmPoweredOffEvent](docs/vim.event.VmPoweredOffEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This event records when a virtual machine has been shut down on an isolated host   in a HA cluster.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| isolatedHost | [vim.event.HostEventArgument](vim.event.HostEventArgument.md "vim.event.HostEventArgument") | None | None | The isolated host on which a virtual machine was shutdown. |
| shutdownResult | string | true | None | Indicates if the shutdown was successful. If the shutdown failed, the virtual   machine was powered off. see Operation |


