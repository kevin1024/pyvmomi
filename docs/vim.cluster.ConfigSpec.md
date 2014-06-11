vim.cluster.ConfigSpec
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
### DEPRECATED



A complete cluster configuration. All fields are defined as   optional. In case of a reconfiguration, unset fields are   unchanged.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| dasConfig | [vim.cluster.DasConfigInfo](vim.cluster.DasConfigInfo.md "vim.cluster.DasConfigInfo") | true | None | Changes to the configuration of vSphere HA. |
| dasVmConfigSpec | [vim.cluster.DasVmConfigSpec](vim.cluster.DasVmConfigSpec.md "vim.cluster.DasVmConfigSpec") | true | None | Changes to the per-virtual-machine vSphere HA settings. |
| drsConfig | [vim.cluster.DrsConfigInfo](vim.cluster.DrsConfigInfo.md "vim.cluster.DrsConfigInfo") | true | None | Changes to the configuration of the VMware DRS service. |
| drsVmConfigSpec | [vim.cluster.DrsVmConfigSpec](vim.cluster.DrsVmConfigSpec.md "vim.cluster.DrsVmConfigSpec") | true | None | Changes to the per-virtual-machine DRS settings. |
| rulesSpec | [vim.cluster.RuleSpec](vim.cluster.RuleSpec.md "vim.cluster.RuleSpec") | true | None | Changes to the set of rules. |


