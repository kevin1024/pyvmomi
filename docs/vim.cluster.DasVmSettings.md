vim.cluster.DasVmSettings
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


The <a href="vim.cluster.DasVmSettings.md">ClusterDasVmSettings</a> data object contains the HA configuration  settings specified for a single virtual machine (identified by  <a href="vim.cluster.DasVmConfigInfo.md">ClusterDasVmConfigInfo</a>.<a href="vim.cluster.DasVmConfigInfo.md#key">key</a>)  or as cluster-wide defaults  (<a href="vim.cluster.DasConfigInfo.md">ClusterDasConfigInfo</a>.<a href="vim.cluster.DasConfigInfo.md#defaultVmSettings">defaultVmSettings</a>).   <p>   All fields are optional. If you set the <code>modify</code>   parameter to <code>true</code> when you call   <a href="vim.ComputeResource.md#reconfigureEx">ReconfigureComputeResource_Task</a>, an unset property has no effect   on the existing property value in the cluster configuration on the Server.   If you set the <code>modify</code> parameter to <code>false</code> when you   reconfigure a cluster, the cluster configuration is reverted to the default   values, then the new configuration values are applied.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| restartPriority | string | true | None | Restart priority for a virtual machine.   <p>   If not specified at either the cluster level or   the virtual machine level, this will default to <code>medium</code>.   <p><br>See <a href="vim.cluster.DasVmSettings.RestartPriority.md">ClusterDasVmSettingsRestartPriority</a><br> |
| isolationResponse | string | true | None | Indicates whether or not the virtual machine should be powered off if a   host determines that it is isolated from the rest of the compute resource.   <p>   If not specified at either the cluster level or   the virtual machine level, this will default to <code>powerOff</code>.   <p><br>See <a href="vim.cluster.DasVmSettings.IsolationResponse.md">ClusterDasVmSettingsIsolationResponse</a><br> |
| vmToolsMonitoringSettings | [vim.cluster.VmToolsMonitoringSettings](vim.cluster.VmToolsMonitoringSettings.md "vim.cluster.VmToolsMonitoringSettings") | true | None | Configuration for the VM Health Monitoring Service. |


