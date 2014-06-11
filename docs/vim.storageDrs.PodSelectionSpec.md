vim.storageDrs.PodSelectionSpec
===============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Specification for moving or copying a virtual machine to a different Storage Pod.   <p>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| initialVmConfig | [vim.storageDrs.PodSelectionSpec.VmPodConfig](vim.storageDrs.PodSelectionSpec.VmPodConfig.md "vim.storageDrs.PodSelectionSpec.VmPodConfig") | true | None | An optional list that allows specifying the storage pod location   for each virtual disk and the VM configurations and overrides to be   used during placement. |
| storagePod | [vim.StoragePod](vim.StoragePod.md "vim.StoragePod") | true | None | The storage pod where the virtual machine should be located. |


