vim.event.DasHostFailedEvent
============================
inherits from [vim.event.ClusterEvent](docs/vim.event.ClusterEvent.md)


This event records when a host failure has been detected by HA.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| failedHost | [vim.event.HostEventArgument](vim.event.HostEventArgument.md "vim.event.HostEventArgument") | None | None | The host that failed. |


