vim.event.EnteringStandbyModeEvent
==================================
inherits from [vim.event.HostEvent](docs/vim.event.HostEvent.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This event records that a host has begun the process of entering   standby mode. All virtual machine operations   are blocked, except the following:   <ul>   <li>MigrateVM   <li>PowerOffVM   <li>SuspendVM   <li>ShutdownGuest   <li>StandbyGuest   </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


