vim.event.DuplicateIpDetectedEvent
==================================
inherits from [vim.event.HostEvent](docs/vim.event.HostEvent.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This event records that a duplicate IP address has been observed in   conflict with the vmotion or IP storage interface configured on the   host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| duplicateIP | string | None | None | The Duplicate IP address detected. |
| macAddress | string | None | None | The MAC associated with duplicate IP. |


