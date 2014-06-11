vim.event.HostWwnConflictEvent
==============================
inherits from [vim.event.HostEvent](docs/vim.event.HostEvent.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This event records a conflict of host WWNs (World Wide Name).

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| conflictedVms | [vim.event.VmEventArgument](vim.event.VmEventArgument.md "vim.event.VmEventArgument") | true | None | The virtual machine whose WWN conflicts with the   current host's WWN. |
| conflictedHosts | [vim.event.HostEventArgument](vim.event.HostEventArgument.md "vim.event.HostEventArgument") | true | None | The host whose physical WWN conflicts with the   current host's WWN. |
| wwn | long | None | None | The WWN in conflict. |


