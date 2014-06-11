vim.event.DvsHostBackInSyncEvent
================================
inherits from [vim.event.DvsEvent](docs/vim.event.DvsEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The DVS configuration on the host was synchronized with that of   the Virtual Center Server and the configuration is the same on   the host and Virtual Center Server.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| hostBackInSync | [vim.event.HostEventArgument](vim.event.HostEventArgument.md "vim.event.HostEventArgument") | None | None | The host that was synchronized. |


