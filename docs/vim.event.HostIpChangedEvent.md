vim.event.HostIpChangedEvent
============================
inherits from [vim.event.HostEvent](docs/vim.event.HostEvent.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This event records a change in host IP address.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| oldIP | string | None | None | Old IP address of the host. |
| newIP | string | None | None | New IP address of the host. |


