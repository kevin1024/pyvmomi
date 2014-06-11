vim.host.FirewallConfig.RuleSetConfig
=====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| rulesetId | string | None | None | Id of the ruleset. |
| enabled | bool | None | None | Flag indicating if the specified ruleset should be enabled. |
| allowedHosts | [vim.host.Ruleset.IpList](vim.host.Ruleset.IpList.md "vim.host.Ruleset.IpList") | true | None | The list of allowed ip addresses |


