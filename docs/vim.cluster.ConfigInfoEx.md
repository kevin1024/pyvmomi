vim.cluster.ConfigInfoEx
========================
inherits from [vim.ComputeResource.ConfigInfo](docs/vim.ComputeResource.ConfigInfo.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


The <a href="vim.cluster.ConfigInfoEx.md">ClusterConfigInfoEx</a> data object describes a complete cluster   configuration. For information about configuring a cluster, see   <a href="vim.cluster.ConfigSpecEx.md">ClusterConfigSpecEx</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| dasConfig | [vim.cluster.DasConfigInfo](vim.cluster.DasConfigInfo.md "vim.cluster.DasConfigInfo") | None | None | Cluster-wide configuration of the vSphere HA service. |
| dasVmConfig | [vim.cluster.DasVmConfigInfo](vim.cluster.DasVmConfigInfo.md "vim.cluster.DasVmConfigInfo") | true | None | List of virtual machine configurations for the vSphere HA   service. Each entry applies to one virtual machine.   <p>   If a virtual machine is not specified in this array, the service uses   the default settings for that virtual machine. |
| drsConfig | [vim.cluster.DrsConfigInfo](vim.cluster.DrsConfigInfo.md "vim.cluster.DrsConfigInfo") | None | None | Cluster-wide configuration of the VMware DRS service. |
| drsVmConfig | [vim.cluster.DrsVmConfigInfo](vim.cluster.DrsVmConfigInfo.md "vim.cluster.DrsVmConfigInfo") | true | None | List of virtual machine configurations for the VMware DRS   service. Each entry applies to one virtual machine.   <p>   If a virtual machine is not specified in this array, the service uses   the default settings for that virtual machine. |
| rule | [vim.cluster.RuleInfo](vim.cluster.RuleInfo.md "vim.cluster.RuleInfo") | true | None | Cluster-wide rules. |
| dpmConfigInfo | [vim.cluster.DpmConfigInfo](vim.cluster.DpmConfigInfo.md "vim.cluster.DpmConfigInfo") | true | None | Cluster-wide configuration of the VMware DPM service. |
| dpmHostConfig | [vim.cluster.DpmHostConfigInfo](vim.cluster.DpmHostConfigInfo.md "vim.cluster.DpmHostConfigInfo") | true | None | List of host configurations for the VMware DPM   service. Each entry applies to one host.   <p>   If a host is not specified in this array, the service uses   the cluster default settings for that host. |
| vsanConfigInfo | [vim.vsan.cluster.ConfigInfo](vim.vsan.cluster.ConfigInfo.md "vim.vsan.cluster.ConfigInfo") | true | None | Cluster-wide configuration of the VMware VSAN service. |
| vsanHostConfig | [vim.vsan.host.ConfigInfo](vim.vsan.host.ConfigInfo.md "vim.vsan.host.ConfigInfo") | true | None | List of host configurations for the VMware VSAN service.  Each entry applies to one host.  <p>  If a host is not specified in this array, the service uses  the cluster default settings for that host. |
| group | [vim.cluster.GroupInfo](vim.cluster.GroupInfo.md "vim.cluster.GroupInfo") | true | None | Cluster-wide groups. |


