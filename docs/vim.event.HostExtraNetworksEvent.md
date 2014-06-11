vim.event.HostExtraNetworksEvent
================================
inherits from [vim.event.HostDasEvent](docs/vim.event.HostDasEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)
### DEPRECATED



This event records the fact that a host has extra networks not used by  other hosts for HA communication

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ips | string | true | None | The comma-separated list of extra networks |


