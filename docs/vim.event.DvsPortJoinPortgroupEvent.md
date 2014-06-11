vim.event.DvsPortJoinPortgroupEvent
===================================
inherits from [vim.event.DvsEvent](docs/vim.event.DvsEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


A port was moved into the distributed virtual portgroup.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| portKey | string | None | None | The port key. |
| portgroupKey | string | None | None | The portgroup key. |
| portgroupName | string | None | None | The portgroup name. |


