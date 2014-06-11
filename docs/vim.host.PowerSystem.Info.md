vim.host.PowerSystem.Info
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Power System Info data object.      Shows current state of power management system.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| currentPolicy | [vim.host.PowerSystem.PowerPolicy](vim.host.PowerSystem.PowerPolicy.md "vim.host.PowerSystem.PowerPolicy") | None | None | Currently selected host power management policy.    This property can have one of the values from    <a href="vim.host.PowerSystem.Capability.md#availablePolicy">availablePolicy</a>. |


