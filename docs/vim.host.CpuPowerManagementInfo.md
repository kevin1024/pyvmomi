vim.host.CpuPowerManagementInfo
===============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The CpuPowerManagementInfo data object type describes supported   power management and current policy.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| currentPolicy | string | true | None | Information about current CPU power management policy. |
| hardwareSupport | string | true | None | Information about supported CPU power management. |


