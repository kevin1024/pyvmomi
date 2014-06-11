vim.dvs.TrafficRuleset
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This class defines a ruleset(set of rules) that will be    applied to network traffic.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | true | None | The key of the ruleset. |
| enabled | bool | true | None | Whether ruleset is enabled or not. |
| precedence | int | true | None | Precedence of the ruleset. Rulesets for a port will be executed    in the order of their precedence. |
| rules | [vim.dvs.TrafficRule](vim.dvs.TrafficRule.md "vim.dvs.TrafficRule") | true | None | List of rules belonging to this ruleset. |


