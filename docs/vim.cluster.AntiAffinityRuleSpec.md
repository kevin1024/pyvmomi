vim.cluster.AntiAffinityRuleSpec
================================
inherits from [vim.cluster.RuleInfo](docs/vim.cluster.RuleInfo.md)


The <a href="vim.cluster.AntiAffinityRuleSpec.md">ClusterAntiAffinityRuleSpec</a> data object defines  a set of virtual machines. DRS will attempt to schedule the virtual  machines to run on different hosts.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vm | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | None | None | List of virtual machine references. |


