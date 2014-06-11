vim.event.DvsPortRuntimeChangeEvent
===================================
inherits from [vim.event.DvsEvent](docs/vim.event.DvsEvent.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


A port of which runtime information is changed in the vNetwork Distributed   Switch.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| portKey | string | None | None | The port key. |
| runtimeInfo | [vim.dvs.DistributedVirtualPort.RuntimeInfo](vim.dvs.DistributedVirtualPort.RuntimeInfo.md "vim.dvs.DistributedVirtualPort.RuntimeInfo") | None | None | The new port runtime information. |


