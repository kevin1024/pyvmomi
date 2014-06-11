vim.cluster.DasVmConfigInfo
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The <a href="vim.cluster.DasVmConfigInfo.md">ClusterDasVmConfigInfo</a> data object contains   the HA configuration for a single virtual machine.   <p>   All fields are optional. If you set the <code>modify</code>   parameter to <code>true</code> when you call   <a href="vim.ComputeResource.md#reconfigureEx">ReconfigureComputeResource_Task</a>, an unset property has no effect   on the existing property value in the cluster configuration on the Server.   If you set the <code>modify</code> parameter to <code>false</code> when you   reconfigure a cluster, the cluster configuration is reverted to the default   values, then the new configuration values are applied.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | None | None | Reference to the virtual machine. |
| restartPriority | [vim.cluster.DasVmConfigInfo.Priority](vim.cluster.DasVmConfigInfo.Priority.md "vim.cluster.DasVmConfigInfo.Priority") | true | None | Restart priority for a virtual machine.    <p>   If there is nothing specified here, then the defaults are picked up from    <a href="vim.cluster.DasConfigInfo.md#defaultVmSettings">defaultVmSettings</a>. |
| powerOffOnIsolation | bool | true | None | Flag to indicate whether or not the virtual machine should be powered off if a   host determines that it is isolated from the rest of the compute resource.   <p>   If there is nothing specified here, then the defaults are picked up from    <a href="vim.cluster.DasConfigInfo.md#defaultVmSettings">defaultVmSettings</a>.   <p> |
| dasSettings | [vim.cluster.DasVmSettings](vim.cluster.DasVmSettings.md "vim.cluster.DasVmSettings") | true | None | HA settings that apply to this virtual machine.   <p>   Values specified in this object override the cluster-wide   defaults for virtual machines (<a href="vim.cluster.DasConfigInfo.md#defaultVmSettings">defaultVmSettings</a>). |


