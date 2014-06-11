vim.cluster.VmGroup
===================
inherits from [vim.cluster.GroupInfo](docs/vim.cluster.GroupInfo.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


The <a href="vim.cluster.VmGroup.md">ClusterVmGroup</a> data object identifies virtual machines  for VM-Host rules. VM-Host rules determine placement of virtual machines  on hosts in a cluster.  The logic specified in a <a href="vim.cluster.VmHostRuleInfo.md">ClusterVmHostRuleInfo</a> object  determines where virtual machines can be powered-on.  <p>  If a virtual machine is removed from the cluster, it loses its DRS group  affiliation. The Server does not restore any group affiliations if the  virtual machine is returned to the cluster.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vm | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | true | None | List of virtual machines that are part of this group.  A virtual machine group can contain zero or more virtual machines. |


