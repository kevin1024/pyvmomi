vim.cluster.VmHostRuleInfo
==========================
inherits from [vim.cluster.RuleInfo](docs/vim.cluster.RuleInfo.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


<p>  A <a href="vim.cluster.VmHostRuleInfo.md">ClusterVmHostRuleInfo</a> object identifies virtual machines  and host groups that determine virtual machine placement. The virtual  machines and hosts referenced by a VM-Host rule must be in the same cluster.  <p>  A VM-Host rule identifies the following groups.  <ul>  <li>A virtual machine group (<a href="vim.cluster.VmGroup.md">ClusterVmGroup</a>).  <li>Two host groups - an affine host group and an anti-affine host group      (<a href="vim.cluster.HostGroup.md">ClusterHostGroup</a>).      At least one of the groups must contain one or more hosts.  </ul>  <p>  <a href="vim.cluster.VmHostRuleInfo.md">ClusterVmHostRuleInfo</a> stores only the names of the relevant  virtual machine and host groups. The group contents are stored in  the virtual machine and host group objects.  <p>  When you modify a VM-Host rule, only the fields that are specified are set.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vmGroupName | string | true | None | Virtual group name (<a href="vim.cluster.VmGroup.md">ClusterVmGroup</a>.<a href="vim.cluster.GroupInfo.md#name">name</a>).  The virtual group may contain one or more virtual machines. |
| affineHostGroupName | string | true | None | Name of the affine host group  (<a href="vim.cluster.HostGroup.md">ClusterHostGroup</a>.<a href="vim.cluster.GroupInfo.md#name">name</a>).  The affine host group identifies hosts on which  <a href="vim.cluster.VmHostRuleInfo.md#vmGroupName">vmGroupName</a> virtual machines can be powered-on.  The value of the <a href="vim.cluster.RuleInfo.md#mandatory">mandatory</a> property  determines how the Server interprets the rule. |
| antiAffineHostGroupName | string | true | None | Name of the anti-affine host group  (<a href="vim.cluster.HostGroup.md">ClusterHostGroup</a>.<a href="vim.cluster.GroupInfo.md#name">name</a>).  The anti-affine host group identifies hosts on which   <a href="vim.cluster.VmHostRuleInfo.md#vmGroupName">vmGroupName</a> virtual machines should not  be powered-on.  The value of the <a href="vim.cluster.RuleInfo.md#mandatory">mandatory</a> property  determines how the Server interprets the rule. |


