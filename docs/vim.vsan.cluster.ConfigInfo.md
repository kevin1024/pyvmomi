vim.vsan.cluster.ConfigInfo
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


The <a href="vim.vsan.cluster.ConfigInfo.md">VsanClusterConfigInfo</a> data object contains configuration  data for the VSAN service in a cluster.  This data object is used both for  specifying cluster-wide settings when updating the VSAN service, and as an  output datatype when retrieving current cluster-wide VSAN service settings.<br>See <a href="vim.ComputeResource.md#reconfigureEx">ReconfigureComputeResource_Task</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| enabled | bool | true | None | Whether the VSAN service is enabled for the cluster. |
| defaultConfig | [vim.vsan.cluster.ConfigInfo.HostDefaultInfo](vim.vsan.cluster.ConfigInfo.HostDefaultInfo.md "vim.vsan.cluster.ConfigInfo.HostDefaultInfo") | true | None | Default VSAN settings to use for hosts admitted to the cluster when the  VSAN service is enabled.  If omitted, values will default as though the  fields in the HostDefaultInfo have been omitted.<br>See <a href="vim.vsan.cluster.ConfigInfo.md#enabled">enabled</a><br>See HostDefaultInfo |


