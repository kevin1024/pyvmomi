vim.vsan.host.ConfigInfo.StorageInfo
====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


Host-local VSAN storage configuration.  This data object is used  both for specifying and retrieving storage configuration for a  host participating in the VSAN service.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| autoClaimStorage | bool | true | None | Whether the VSAN service is configured to automatically claim local  unused storage on this host.   When set, the VSAN service will automatically format and use local  disks.  Side effects from any disk consumption will be reflected in  <a href="vim.vsan.host.ConfigInfo.StorageInfo.md#diskMapping">diskMapping</a>.   If this argument is specified as a host-level configuration input  at the VC-level (see <a href="vim.cluster.ConfigInfoEx.md#vsanHostConfig">vsanHostConfig</a>),  it will override that of any cluster-level default value.<br>See <a href="vim.vsan.host.ConfigInfo.StorageInfo.md#diskMapping">diskMapping</a><br>See <a href="vim.cluster.ConfigInfoEx.md#vsanHostConfig">vsanHostConfig</a><br>See <a href="vim.vsan.cluster.ConfigInfo.md#defaultConfig">defaultConfig</a><br> |
| diskMapping | [vim.vsan.host.DiskMapping](vim.vsan.host.DiskMapping.md "vim.vsan.host.DiskMapping") | true | None | List of <a href="vim.vsan.host.DiskMapping.md">VsanHostDiskMapping</a> entries in use by the VSAN service.   DiskMappings to be used by the VSAN service may be manually  specified using  vim.host.VsanSystem#initializeDisks(DiskMapping[]).<br>See vim.host.VsanSystem#initializeDisks(DiskMapping[]) |


