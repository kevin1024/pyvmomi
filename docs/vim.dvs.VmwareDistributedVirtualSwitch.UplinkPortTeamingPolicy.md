vim.dvs.VmwareDistributedVirtualSwitch.UplinkPortTeamingPolicy
==============================================================
inherits from [vim.InheritablePolicy](docs/vim.InheritablePolicy.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Policy for a uplink port team.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| policy | [vim.StringPolicy](vim.StringPolicy.md "vim.StringPolicy") | true | None | Network adapter teaming policy. The policy defines the way traffic    from the clients of the team is routed through the different uplinks    in the team. The policies supported on the VDS platform is one of    <a href="vim.DistributedVirtualSwitch.FeatureCapability.md#nicTeamingPolicy">nicTeamingPolicy</a>. |
| reversePolicy | [vim.BoolPolicy](vim.BoolPolicy.md "vim.BoolPolicy") | true | None | The flag to indicate whether or not the teaming policy is applied   to inbound frames as well. Also see <a href="vim.host.NetworkPolicy.NicTeamingPolicy.md#reversePolicy">reversePolicy</a> |
| notifySwitches | [vim.BoolPolicy](vim.BoolPolicy.md "vim.BoolPolicy") | true | None | Flag to specify whether or not to notify the physical switch   if a link fails. Also see <a href="vim.host.NetworkPolicy.NicTeamingPolicy.md#notifySwitches">notifySwitches</a> |
| rollingOrder | [vim.BoolPolicy](vim.BoolPolicy.md "vim.BoolPolicy") | true | None | The flag to indicate whether or not to use a rolling policy when   restoring links. Also see <a href="vim.host.NetworkPolicy.NicTeamingPolicy.md#rollingOrder">rollingOrder</a> |
| failureCriteria | [vim.dvs.VmwareDistributedVirtualSwitch.FailureCriteria](vim.dvs.VmwareDistributedVirtualSwitch.FailureCriteria.md "vim.dvs.VmwareDistributedVirtualSwitch.FailureCriteria") | true | None | Failover detection policy for the uplink port team. |
| uplinkPortOrder | [vim.dvs.VmwareDistributedVirtualSwitch.UplinkPortOrderPolicy](vim.dvs.VmwareDistributedVirtualSwitch.UplinkPortOrderPolicy.md "vim.dvs.VmwareDistributedVirtualSwitch.UplinkPortOrderPolicy") | true | None | Failover order policy for uplink ports on the hosts. |


