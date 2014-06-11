vim.event.HostCnxFailedAlreadyManagedEvent
==========================================
inherits from [vim.event.HostEvent](docs/vim.event.HostEvent.md)


This event records a failure to connect to a host   due to the host being managed by a different VirtualCenter server.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| serverName | string | None | None | The name of the VirtualCenter server that manages the host. |


