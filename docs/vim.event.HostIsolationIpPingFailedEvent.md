vim.event.HostIsolationIpPingFailedEvent
========================================
inherits from [vim.event.HostDasEvent](docs/vim.event.HostDasEvent.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This event records that the isolation address could not be pinged.   The default isolation address is the service console's default gateway.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| isolationIp | string | None | None |  |


