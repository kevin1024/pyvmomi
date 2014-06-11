vim.event.GhostDvsProxySwitchRemovedEvent
=========================================
inherits from [vim.event.HostEvent](docs/vim.event.HostEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This event records when the ghost DVS proxy switches (a.k.a host   proxy switches that don't match any DVS defined in Virtual Center)   were removed on the host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| switchUuid | string | None | None | The list of ghost DVS proxy switch uuid that were removed. |


