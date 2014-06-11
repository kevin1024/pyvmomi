vim.event.UnlicensedVirtualMachinesEvent
========================================
inherits from [vim.event.LicenseEvent](docs/vim.event.LicenseEvent.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This event records that we have unlicensed virtual machines on the  specified host. This can be both a (@link vim.ManagedEntity.configIssue  configIssue) and an entry in the event log.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| unlicensed | int | None | None |  |
| available | int | None | None |  |


