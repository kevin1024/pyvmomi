vim.cluster.DrsConfigInfo
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The <a href="vim.cluster.DrsConfigInfo.md">ClusterDrsConfigInfo</a> data object contains configuration information   for the VMware DRS service.   <p>   All fields are optional. If you set the <code>modify</code>   parameter to <code>true</code> when you call   <a href="vim.ComputeResource.md#reconfigureEx">ReconfigureComputeResource_Task</a>, an unset property has no effect   on the existing property value in the cluster configuration on the Server.   If you set the <code>modify</code> parameter to <code>false</code> when you   reconfigure a cluster, the cluster configuration is reverted to the default   values, then the new configuration values are applied.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| enabled | bool | true | None | Flag indicating whether or not the service is enabled. |
| enableVmBehaviorOverrides | bool | true | None | Flag that dictates whether DRS Behavior overrides for individual   virtual machines (<a href="vim.cluster.DrsVmConfigInfo.md">ClusterDrsVmConfigInfo</a>) are enabled. The default   value is <code>true</code>.   <p>   When this flag is <code>true</code>, the   <a href="vim.cluster.ConfigSpecEx.md">ClusterConfigSpecEx</a>.<a href="vim.cluster.ConfigSpecEx.md#drsVmConfigSpec">drsVmConfigSpec</a>   values override the <a href="vim.cluster.DrsConfigInfo.md#defaultVmBehavior">defaultVmBehavior</a>.   <p>   When this flag is <code>false</code>, the   <a href="vim.cluster.DrsConfigInfo.md#defaultVmBehavior">defaultVmBehavior</a> value applies to all virtual   machines, with the following exception: in a cluster that has EVC disabled,   you cannot override the virtual machine setting   (<a href="vim.cluster.ConfigSpecEx.md#drsVmConfigSpec">drsVmConfigSpec</a>)   for Fault Tolerance virtual machines. |
| defaultVmBehavior | [vim.cluster.DrsConfigInfo.DrsBehavior](vim.cluster.DrsConfigInfo.DrsBehavior.md "vim.cluster.DrsConfigInfo.DrsBehavior") | true | None | Specifies the cluster-wide default DRS behavior for virtual machines.   You can override the default behavior for a virtual machine   by using the <a href="vim.cluster.DrsVmConfigInfo.md">ClusterDrsVmConfigInfo</a> object. |
| vmotionRate | int | true | None | Threshold for generated <a href="vim.cluster.Recommendation.md">ClusterRecommendation</a>s.   DRS generates only those recommendations that are above the   specified vmotionRate. Ratings vary from 1 to 5. This setting applies   to manual, partiallyAutomated, and fullyAutomated   DRS clusters. See <a href="vim.cluster.DrsConfigInfo.DrsBehavior.md">DrsBehavior</a>. |
| option | [vim.option.OptionValue](vim.option.OptionValue.md "vim.option.OptionValue") | true | None | Advanced settings. |


