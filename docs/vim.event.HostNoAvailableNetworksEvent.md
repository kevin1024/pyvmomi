vim.event.HostNoAvailableNetworksEvent
======================================
inherits from [vim.event.HostDasEvent](docs/vim.event.HostDasEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This event records the fact that a host does not have any available networks  for HA communication

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ips | string | true | None | The comma-separated list of used networks |


