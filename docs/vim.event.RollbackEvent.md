vim.event.RollbackEvent
=======================
inherits from [vim.event.DvsEvent](docs/vim.event.DvsEvent.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


This event is generated when network configuration rollback   occurs on a host due configuration change that disconnected  the host from vSphere server

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| hostName | string | None | None | The host on which rollback happened |
| methodName | string | true | None | The API method that was rolled back |


