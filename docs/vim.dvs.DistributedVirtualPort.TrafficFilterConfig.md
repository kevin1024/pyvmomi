vim.dvs.DistributedVirtualPort.TrafficFilterConfig
==================================================
inherits from [vim.dvs.DistributedVirtualPort.FilterConfig](docs/vim.dvs.DistributedVirtualPort.FilterConfig.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This class defines Traffic Filter configuration.   <p> <b> Supported Qualifier and Actions </b>   <table border="1" width="100%">   <tr>      <th>Traffic Filter Config</th>      <th>Supported classes</th>   </tr>    <tr>      <td>Qualifiers supported</td>      <td><a href="vim.SingleIp.md">SingleIp</a>, <a href="vim.IpRange.md">IpRange</a>,          <a href="vim.SingleMac.md">SingleMac</a>, <a href="vim.MacRange.md">MacRange</a>,          <a href="vim.dvs.TrafficRule.SingleIpPort.md">DvsSingleIpPort</a>,          <a href="vim.dvs.TrafficRule.SystemTrafficQualifier.md">DvsSystemTrafficNetworkRuleQualifier</a>      </td>   </tr>    <tr>      <td>Actions Supported</td>      <td><a href="vim.dvs.TrafficRule.DropAction.md">DvsDropNetworkRuleAction</a>,          <a href="vim.dvs.TrafficRule.AcceptAction.md">DvsAcceptNetworkRuleAction</a>,          <a href="vim.dvs.TrafficRule.PuntAction.md">DvsPuntNetworkRuleAction</a>,          <a href="vim.dvs.TrafficRule.CopyAction.md">DvsCopyNetworkRuleAction</a>,          <a href="vim.dvs.TrafficRule.MacRewriteAction.md">DvsMacRewriteNetworkRuleAction</a>,          <a href="vim.dvs.TrafficRule.GreAction.md">DvsGreEncapNetworkRuleAction</a>,          <a href="vim.dvs.TrafficRule.LogAction.md">DvsLogNetworkRuleAction</a>,          <a href="vim.dvs.TrafficRule.UpdateTagAction.md">DvsUpdateTagNetworkRuleAction</a>,          <a href="vim.dvs.TrafficRule.RateLimitAction.md">DvsRateLimitNetworkRuleAction</a>      </td>   </tr>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| trafficRuleset | [vim.dvs.TrafficRuleset](vim.dvs.TrafficRuleset.md "vim.dvs.TrafficRuleset") | true | None | Network Traffic Ruleset |


