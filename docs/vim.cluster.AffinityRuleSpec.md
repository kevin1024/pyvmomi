vim.cluster.AffinityRuleSpec
============================
inherits from [vim.cluster.RuleInfo](docs/vim.cluster.RuleInfo.md)


The <a href="vim.cluster.AffinityRuleSpec.md">ClusterAffinityRuleSpec</a> data object defines a set   of virtual machines. DRS will attempt to schedule the virtual machines   to run on the same host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vm | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | None | None | List of virtual machine references. |


