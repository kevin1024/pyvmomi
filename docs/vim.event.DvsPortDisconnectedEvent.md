vim.event.DvsPortDisconnectedEvent
==================================
inherits from [vim.event.DvsEvent](docs/vim.event.DvsEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


A port is disconnected in the distributed virtual switch.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| portKey | string | None | None | The port key. |
| connectee | [vim.dvs.PortConnectee](vim.dvs.PortConnectee.md "vim.dvs.PortConnectee") | true | None | The port's formal connectee. |


