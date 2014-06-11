vim.event.DvsMergedEvent
========================
inherits from [vim.event.DvsEvent](docs/vim.event.DvsEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Two distributed virtual switches was merged.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| sourceDvs | [vim.event.DvsEventArgument](vim.event.DvsEventArgument.md "vim.event.DvsEventArgument") | None | None | The source DVS. |
| destinationDvs | [vim.event.DvsEventArgument](vim.event.DvsEventArgument.md "vim.event.DvsEventArgument") | None | None | The destination DVS. |


