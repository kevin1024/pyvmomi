vim.storageDrs.PodSelectionSpec.VmPodConfig
===========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Initial VM configuration for the specified pod.   This configuration will be saved to the pod config   <a href="vim.storageDrs.ConfigInfo.md">StorageDrsConfigInfo</a>   when the placement recommendations are applied.   <p>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| storagePod | [vim.StoragePod](vim.StoragePod.md "vim.StoragePod") | None | None | The pod that this initial configuration applies to.  Since there could be multiple pods in a single placement request,  we may need to specify multiple initial VM configurations, one per  pod. |
| disk | [vim.storageDrs.PodSelectionSpec.DiskLocator](vim.storageDrs.PodSelectionSpec.DiskLocator.md "vim.storageDrs.PodSelectionSpec.DiskLocator") | true | None | Array of PodDiskLocator objects. |
| vmConfig | [vim.storageDrs.VmConfigInfo](vim.storageDrs.VmConfigInfo.md "vim.storageDrs.VmConfigInfo") | true | None | The VM configuration for the VM that is being placed. |
| interVmRule | [vim.cluster.RuleInfo](vim.cluster.RuleInfo.md "vim.cluster.RuleInfo") | true | None | The initial interVmRules that should during placement of this  virtual machine. It may not always be possible to specify that the  virtual machine being placed is part of the rule because the  virtual machine may not have been created yet. So for simplicity,  we assume the virtual machine being placed is always implicitly  part of any rule specified. It will be explicitly added to the  rule before it is saved to the pod config. |


