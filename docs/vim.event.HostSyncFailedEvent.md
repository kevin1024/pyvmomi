vim.event.HostSyncFailedEvent
=============================
inherits from [vim.event.HostEvent](docs/vim.event.HostEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This event records a failure to sync up with the VirtualCenter agent on the host

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| reason | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | None | None | The reason for the failure. |


