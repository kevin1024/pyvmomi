vim.host.AutoStartManager.Config
================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Contains the entire auto-start/auto-stop configuration.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| defaults | [vim.host.AutoStartManager.SystemDefaults](vim.host.AutoStartManager.SystemDefaults.md "vim.host.AutoStartManager.SystemDefaults") | true | None | System defaults for auto-start/auto-stop. |
| powerInfo | [vim.host.AutoStartManager.AutoPowerInfo](vim.host.AutoStartManager.AutoPowerInfo.md "vim.host.AutoStartManager.AutoPowerInfo") | true | None | Lists the auto-start/auto-stop configuration. If a virtual machine is not   mentioned in this array, it does not participate in auto-start/auto-stop   operations. |


