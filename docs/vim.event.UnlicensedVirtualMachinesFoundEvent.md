vim.event.UnlicensedVirtualMachinesFoundEvent
=============================================
inherits from [vim.event.LicenseEvent](docs/vim.event.LicenseEvent.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This event records that we discovered unlicensed virtual machines on  the specified host. After this event is entered into the event log, we  expect to see a corresponding (@link  vim.event.Event.UnlicensedVirtualMachinesEvent  UnlicensedVirtualMachinesEvent) (@link vim.ManagedEntity.configIssue  configIssue) on the host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| available | int | None | None |  |


