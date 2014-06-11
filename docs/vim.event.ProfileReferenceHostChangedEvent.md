vim.event.ProfileReferenceHostChangedEvent
==========================================
inherits from [vim.event.ProfileEvent](docs/vim.event.ProfileEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This event records that the reference host associated with this profile has changed

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| referenceHost | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | true | None | The newly associated reference host with this profile |


