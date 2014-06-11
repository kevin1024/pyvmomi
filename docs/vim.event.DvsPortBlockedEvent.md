vim.event.DvsPortBlockedEvent
=============================
inherits from [vim.event.DvsEvent](docs/vim.event.DvsEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


A port is blocked in the distributed virtual switch.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| portKey | string | None | None | The port key. |
| statusDetail | string | true | None | Reason for port's current status |
| runtimeInfo | [vim.dvs.DistributedVirtualPort.RuntimeInfo](vim.dvs.DistributedVirtualPort.RuntimeInfo.md "vim.dvs.DistributedVirtualPort.RuntimeInfo") | true | None | The port runtime information. |


