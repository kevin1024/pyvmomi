vim.dvs.VmwareDistributedVirtualSwitch.VMwarePortgroupPolicy
============================================================
inherits from [vim.dvs.DistributedVirtualPortgroup.PortgroupPolicy](docs/vim.dvs.DistributedVirtualPortgroup.PortgroupPolicy.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This class defines the VMware specific configuration for   DistributedVirtualPort.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vlanOverrideAllowed | bool | None | None | Allow the setting of   <a href="vim.dvs.VmwareDistributedVirtualSwitch.VlanIdSpec.md#vlanId">vlanId</a>, trunk   <a href="vim.dvs.VmwareDistributedVirtualSwitch.TrunkVlanSpec.md#vlanId">vlanId</a>, or   <a href="vim.dvs.VmwareDistributedVirtualSwitch.PvlanSpec.md#pvlanId">pvlanId</a>   for an individual port to override the setting in   <a href="vim.dvs.DistributedVirtualPortgroup.ConfigInfo.md#defaultPortConfig">defaultPortConfig</a> of   a portgroup. |
| uplinkTeamingOverrideAllowed | bool | None | None | Allow the setting of   <a href="vim.dvs.VmwareDistributedVirtualSwitch.VmwarePortConfigPolicy.md#uplinkTeamingPolicy">uplinkTeamingPolicy</a>   for an individual port to override the setting in   <a href="vim.dvs.DistributedVirtualPortgroup.ConfigInfo.md#defaultPortConfig">defaultPortConfig</a> of   a portgroup. |
| securityPolicyOverrideAllowed | bool | None | None | Allow the setting of   <a href="vim.dvs.VmwareDistributedVirtualSwitch.VmwarePortConfigPolicy.md#securityPolicy">securityPolicy</a>   for an individual port to override the setting in   <a href="vim.dvs.DistributedVirtualPortgroup.ConfigInfo.md#defaultPortConfig">defaultPortConfig</a> of   a portgroup. |
| ipfixOverrideAllowed | bool | true | None | Allow the setting of   <a href="vim.dvs.VmwareDistributedVirtualSwitch.VmwarePortConfigPolicy.md#ipfixEnabled">ipfixEnabled</a>   for an individual port to override the setting in   <a href="vim.dvs.DistributedVirtualPortgroup.ConfigInfo.md#defaultPortConfig">defaultPortConfig</a> of   a portgroup. |


