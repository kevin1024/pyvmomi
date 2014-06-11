vim.event.HostShortNameInconsistentEvent
========================================
inherits from [vim.event.HostDasEvent](docs/vim.event.HostDasEvent.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)
### DEPRECATED



This event records that host name resolution returned different names on  the host. Please check your host's network configuration and your DNS  configuration. There may be duplicate entries.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| shortName | string | None | None |  |
| shortName2 | string | None | None |  |


