vim.event.DvsPortEnteredPassthruEvent
=====================================
inherits from [vim.event.DvsEvent](docs/vim.event.DvsEvent.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


A port has entered passthrough mode on the distributed virtual switch.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| portKey | string | None | None | The port key. |
| runtimeInfo | [vim.dvs.DistributedVirtualPort.RuntimeInfo](vim.dvs.DistributedVirtualPort.RuntimeInfo.md "vim.dvs.DistributedVirtualPort.RuntimeInfo") | true | None | The port runtime information. |


