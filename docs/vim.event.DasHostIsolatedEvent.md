vim.event.DasHostIsolatedEvent
==============================
inherits from [vim.event.ClusterEvent](docs/vim.event.ClusterEvent.md)


This event records that a host has been isolated from the network in a  HA cluster. Since an isolated host cannot be distinguished from a failed  host except by the isolated host itself, this event is logged when the  isolated host regains network connectivity.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| isolatedHost | [vim.event.HostEventArgument](vim.event.HostEventArgument.md "vim.event.HostEventArgument") | None | None | The host that was isolated. |


