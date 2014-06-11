vim.cluster.HostGroup
=====================
inherits from [vim.cluster.GroupInfo](docs/vim.cluster.GroupInfo.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


The <a href="vim.cluster.HostGroup.md">ClusterHostGroup</a> data object identifies hosts for VM-Host rules.   VM-Host rules determine placement of virtual machines on hosts in a cluster.   The logic specified in a <a href="vim.cluster.VmHostRuleInfo.md">ClusterVmHostRuleInfo</a> object   determines where virtual machines can be powered-on.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| host | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | true | None | List of hosts that are part of this group.   A host group can contain zero or more hosts. |


