vim.dvs.TrafficRule.SystemTrafficQualifier
==========================================
inherits from [vim.dvs.TrafficRule.Qualifier](docs/vim.dvs.TrafficRule.Qualifier.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This class defines the System Traffic Qualifier. Here the type of    traffic will be used for classifying packets.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| typeOfSystemTraffic | [vim.StringExpression](vim.StringExpression.md "vim.StringExpression") | true | None | Type of system traffic.    See <a href="vim.DistributedVirtualSwitch.HostInfrastructureTrafficClass.md">DistributedVirtualSwitchHostInfrastructureTrafficClass</a>    for valid values. |


