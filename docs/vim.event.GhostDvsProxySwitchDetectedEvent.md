vim.event.GhostDvsProxySwitchDetectedEvent
==========================================
inherits from [vim.event.HostEvent](docs/vim.event.HostEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This event records when Virtual Center server found DVS proxy switches   on the host that don't match any DVS defined in Virtual Center.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| switchUuid | string | None | None | The list of ghost DVS proxy switch uuids that were found. |


