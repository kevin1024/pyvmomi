vim.event.HostLocalPortCreatedEvent
===================================
inherits from [vim.event.DvsEvent](docs/vim.event.DvsEvent.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


This event records when host local port is created to recover from   management network connectivity loss.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| hostLocalPort | [vim.dvs.DistributedVirtualPort.HostLocalPortInfo](vim.dvs.DistributedVirtualPort.HostLocalPortInfo.md "vim.dvs.DistributedVirtualPort.HostLocalPortInfo") | None | None | The configuration of the new host local port. |


