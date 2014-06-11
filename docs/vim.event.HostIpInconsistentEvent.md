vim.event.HostIpInconsistentEvent
=================================
inherits from [vim.event.HostEvent](docs/vim.event.HostEvent.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)
### DEPRECATED



This event records that the IP address resolution returned different   addresses on the host.  Please check your host's network configuration.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ipAddress | string | None | None |  |
| ipAddress2 | string | None | None |  |


