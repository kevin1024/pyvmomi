vim.dvs.TrafficRule
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This class defines a single rule that will be applied to network traffic.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | true | None | The key of the rule |
| description | string | true | None | Description of the rule |
| sequence | int | true | None | Sequence of this rule. i.e, the order in which this rule appears    in the ruleset. |
| qualifier | [vim.dvs.TrafficRule.Qualifier](vim.dvs.TrafficRule.Qualifier.md "vim.dvs.TrafficRule.Qualifier") | true | None | List of Network rule qualifiers. 'AND' of this array of    network rule qualifiers is applied as one network traffic rule.    If the TrafficRule belongs to    <a href="vim.dvs.DistributedVirtualPort.FilterPolicy.md">DvsFilterPolicy</a> :    There can be a maximum of 1 <a href="vim.dvs.TrafficRule.IpQualifier.md">DvsIpNetworkRuleQualifier</a>,    1 <a href="vim.dvs.TrafficRule.MacQualifier.md">DvsMacNetworkRuleQualifier</a> and    1 <a href="vim.dvs.TrafficRule.SystemTrafficQualifier.md">DvsSystemTrafficNetworkRuleQualifier</a> for a total of    3 <a href="vim.dvs.TrafficRule.md#qualifier">qualifier</a>    If the TrafficRule belongs to    <a href="vim.dvs.StatefulFirewallPolicy.md">DvsStatefulFirewallPolicy</a> :    There can be only 1 <a href="vim.dvs.TrafficRule.Qualifier.md">DvsNetworkRuleQualifier</a> in    <a href="vim.dvs.TrafficRule.md#qualifier">qualifier</a> |
| action | [vim.dvs.TrafficRule.Action](vim.dvs.TrafficRule.Action.md "vim.dvs.TrafficRule.Action") | true | None | Action to be applied for this rule. |
| direction | string | true | None | Whether this rule needs to be applied to incoming packets,    to outgoing packets or both.    See RuleDirectionType for valid values. |


