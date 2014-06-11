vim.vsan.host.ConfigInfo
========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


The <a href="vim.vsan.host.ConfigInfo.md">VsanHostConfigInfo</a> data object contains host-specific settings  for the VSAN service.  This data object is used both for specifying  settings for updating the VSAN service, and as an output datatype  when retrieving current VSAN service settings.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| enabled | bool | true | None | Whether the VSAN service is currently enabled on this host. |
| hostSystem | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | true | None | The <a href="vim.HostSystem.md">HostSystem</a> for this host.   This argument is required when this configuration is specified as  an input to VC-level APIs.  When this configuration is specified  to a host-level direct API, this argument may be omitted.<br>See <a href="vim.ComputeResource.md#reconfigureEx">ReconfigureComputeResource_Task</a><br>See <a href="vim.host.VsanSystem.md#update">UpdateVsan_Task</a><br> |
| clusterInfo | [vim.vsan.host.ConfigInfo.ClusterInfo](vim.vsan.host.ConfigInfo.ClusterInfo.md "vim.vsan.host.ConfigInfo.ClusterInfo") | true | None | The VSAN service cluster configuration for this host. |
| storageInfo | [vim.vsan.host.ConfigInfo.StorageInfo](vim.vsan.host.ConfigInfo.StorageInfo.md "vim.vsan.host.ConfigInfo.StorageInfo") | true | None | The VSAN storage configuration for this host.   VSAN storage configuration settings are independent of the  current value of <a href="vim.vsan.host.ConfigInfo.md#enabled">enabled</a>. |
| networkInfo | [vim.vsan.host.ConfigInfo.NetworkInfo](vim.vsan.host.ConfigInfo.NetworkInfo.md "vim.vsan.host.ConfigInfo.NetworkInfo") | true | None | The VSAN network configuration for this host.   VSAN network configuration settings are independent of the  current value of <a href="vim.vsan.host.ConfigInfo.md#enabled">enabled</a>. |


