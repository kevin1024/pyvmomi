vim.event.MigrationResourceErrorEvent
=====================================
inherits from [vim.event.MigrationEvent](docs/vim.event.MigrationEvent.md)


A migration error that includes both the destination host and resource pool.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| dstPool | [vim.event.ResourcePoolEventArgument](vim.event.ResourcePoolEventArgument.md "vim.event.ResourcePoolEventArgument") | None | None | The name of the destination resource pool. |
| dstHost | [vim.event.HostEventArgument](vim.event.HostEventArgument.md "vim.event.HostEventArgument") | None | None | The name of the destination host. |


