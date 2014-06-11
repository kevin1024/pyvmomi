vim.event.DvsHealthStatusChangeEvent
====================================
inherits from [vim.event.HostEvent](docs/vim.event.HostEvent.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


Health check status of an switch is changed.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| switchUuid | string | None | None | UUID of the DVS the host is connected to. |
| healthResult | [vim.dvs.HostMember.HealthCheckResult](vim.dvs.HostMember.HealthCheckResult.md "vim.dvs.HostMember.HealthCheckResult") | true | None | Health check status. |


