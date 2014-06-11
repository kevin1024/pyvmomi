vim.cluster.ConfigInfo
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
### DEPRECATED



A complete cluster configuration.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| dasConfig | [vim.cluster.DasConfigInfo](vim.cluster.DasConfigInfo.md "vim.cluster.DasConfigInfo") | None | None | Cluster-wide configuration of the vSphere HA service. |
| dasVmConfig | [vim.cluster.DasVmConfigInfo](vim.cluster.DasVmConfigInfo.md "vim.cluster.DasVmConfigInfo") | true | None | List of virtual machine configurations for the vSphere HA   service. Each entry applies to one virtual machine.   <p>   If a virtual machine is not specified in this array, the service uses   the default settings for that virtual machine. |
| drsConfig | [vim.cluster.DrsConfigInfo](vim.cluster.DrsConfigInfo.md "vim.cluster.DrsConfigInfo") | None | None | Cluster-wide configuration of the VMware DRS service. |
| drsVmConfig | [vim.cluster.DrsVmConfigInfo](vim.cluster.DrsVmConfigInfo.md "vim.cluster.DrsVmConfigInfo") | true | None | List of virtual machine configurations for the VMware DRS   service. Each entry applies to one virtual machine.   <p>   If a virtual machine is not specified in this array, the service uses   the default settings for that virtual machine. |
| rule | [vim.cluster.RuleInfo](vim.cluster.RuleInfo.md "vim.cluster.RuleInfo") | true | None | Cluster-wide rules. |


