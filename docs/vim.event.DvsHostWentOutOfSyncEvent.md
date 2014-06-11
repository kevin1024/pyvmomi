vim.event.DvsHostWentOutOfSyncEvent
===================================
inherits from [vim.event.DvsEvent](docs/vim.event.DvsEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The DVS configuration on the host diverged from that of   the Virtual Center Server.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| hostOutOfSync | [vim.event.DvsOutOfSyncHostArgument](vim.event.DvsOutOfSyncHostArgument.md "vim.event.DvsOutOfSyncHostArgument") | None | None | The host that went out of sync. |


