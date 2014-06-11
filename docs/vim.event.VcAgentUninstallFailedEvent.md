vim.event.VcAgentUninstallFailedEvent
=====================================
inherits from [vim.event.HostEvent](docs/vim.event.HostEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This event records when the VirtualCenter agent on a host failed to uninstall.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| reason | string | true | None | The reason why the uninstall failed, if known.  See <a href="vim.fault.AgentInstallFailed.Reason.md">AgentInstallFailedReason</a> |


