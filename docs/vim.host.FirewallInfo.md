vim.host.FirewallInfo
=====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Data object describing the firewall configuration.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| defaultPolicy | [vim.host.FirewallInfo.DefaultPolicy](vim.host.FirewallInfo.DefaultPolicy.md "vim.host.FirewallInfo.DefaultPolicy") | None | None | Default firewall policy. |
| ruleset | [vim.host.Ruleset](vim.host.Ruleset.md "vim.host.Ruleset") | true | None | List of configured rulesets. |


