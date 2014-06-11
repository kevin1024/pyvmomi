vim.dvs.DistributedVirtualPort.FilterConfig
===========================================
inherits from [vim.InheritablePolicy](docs/vim.InheritablePolicy.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This class defines Network Filter configuration.   <p> <b> Supported Qualifier and Actions </b>   <table border="1" width="100%">   <tr>      <th>Network Filter Config</th>      <th>Supported classes</th>   </tr>    <tr>      <td>Qualifiers supported</td>      <td><a href="vim.SingleIp.md">SingleIp</a>, <a href="vim.IpRange.md">IpRange</a>,          <a href="vim.SingleMac.md">SingleMac</a>, <a href="vim.MacRange.md">MacRange</a>,          <a href="vim.dvs.TrafficRule.SingleIpPort.md">DvsSingleIpPort</a>,          <a href="vim.dvs.TrafficRule.SystemTrafficQualifier.md">DvsSystemTrafficNetworkRuleQualifier</a>      </td>   </tr>    <tr>      <td>Actions Supported</td>      <td><a href="vim.dvs.TrafficRule.DropAction.md">DvsDropNetworkRuleAction</a>,          <a href="vim.dvs.TrafficRule.AcceptAction.md">DvsAcceptNetworkRuleAction</a>,          <a href="vim.dvs.TrafficRule.PuntAction.md">DvsPuntNetworkRuleAction</a>,          <a href="vim.dvs.TrafficRule.CopyAction.md">DvsCopyNetworkRuleAction</a>,          <a href="vim.dvs.TrafficRule.MacRewriteAction.md">DvsMacRewriteNetworkRuleAction</a>,          <a href="vim.dvs.TrafficRule.GreAction.md">DvsGreEncapNetworkRuleAction</a>,          <a href="vim.dvs.TrafficRule.LogAction.md">DvsLogNetworkRuleAction</a>,          <a href="vim.dvs.TrafficRule.UpdateTagAction.md">DvsUpdateTagNetworkRuleAction</a>,          <a href="vim.dvs.TrafficRule.RateLimitAction.md">DvsRateLimitNetworkRuleAction</a>      </td>   </tr>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | true | None | The key of Network Filter Config. |
| agentName | string | true | None | The name of the network traffic filter agent. |
| slotNumber | string | true | None | The slot number of the network filter agent. |
| parameters | [vim.dvs.DistributedVirtualPort.FilterParameter](vim.dvs.DistributedVirtualPort.FilterParameter.md "vim.dvs.DistributedVirtualPort.FilterParameter") | true | None | Network Filter Parameter |
| onFailure | string | true | None | This property specifies whether to allow all traffic or to deny all   traffic when a Network Filter fails to configure.   Please see <a href="vim.dvs.DistributedVirtualPort.FilterOnFailure.md">DvsFilterOnFailure</a>   for more details. |


