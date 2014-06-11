vim.event.VcAgentUpgradeFailedEvent
===================================
inherits from [vim.event.HostEvent](docs/vim.event.HostEvent.md)


This event records when the VirtualCenter agent on a host failed to upgrade.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| reason | string | true | None | The reason why the upgrade failed, if known.  See <a href="vim.fault.AgentInstallFailed.Reason.md">AgentInstallFailedReason</a> |


