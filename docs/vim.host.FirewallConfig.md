vim.host.FirewallConfig
=======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


DataObject used for firewall configuration

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| rule | [vim.host.FirewallConfig.RuleSetConfig](vim.host.FirewallConfig.RuleSetConfig.md "vim.host.FirewallConfig.RuleSetConfig") | true | None | Rules determining firewall settings. |
| defaultBlockingPolicy | [vim.host.FirewallInfo.DefaultPolicy](vim.host.FirewallInfo.DefaultPolicy.md "vim.host.FirewallInfo.DefaultPolicy") | None | None | Default settings for the firewall,  used for ports that are not explicitly opened. |


