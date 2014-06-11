vim.storageDrs.ConfigInfo
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


The <a href="vim.storageDrs.ConfigInfo.md">StorageDrsConfigInfo</a> data object describes storage DRS configuration   for a pod <a href="vim.StoragePod.md">StoragePod</a>.   <p>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| podConfig | [vim.storageDrs.PodConfigInfo](vim.storageDrs.PodConfigInfo.md "vim.storageDrs.PodConfigInfo") | None | None | Pod-wide configuration of the storage DRS service. |
| vmConfig | [vim.storageDrs.VmConfigInfo](vim.storageDrs.VmConfigInfo.md "vim.storageDrs.VmConfigInfo") | true | None | List of virtual machine configurations for the storage DRS   service. Each entry applies to all the virtual disks of the virtual machine   on this pod.   <p>   If a virtual machine is not specified in this array, the service uses   the default settings for that virtual machine. |


