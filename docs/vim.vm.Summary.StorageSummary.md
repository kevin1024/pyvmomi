vim.vm.Summary.StorageSummary
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


A subset of the storage information of this virtual machine.   <p>   See <a href="vim.vm.StorageInfo.md">VirtualMachineStorageInfo</a> for a detailed storage break-up.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| committed | long | None | None | Total storage space, in bytes, committed to this virtual machine across   all datastores.   <p>   Essentially an aggregate of the property   <a href="vim.vm.StorageInfo.UsageOnDatastore.md#committed">committed</a> across all   datastores that this virtual machine is located on. |
| uncommitted | long | None | None | Additional storage space, in bytes, potentially used by this virtual machine   on all datastores.   <p>   Essentially an aggregate of the property   <a href="vim.vm.StorageInfo.UsageOnDatastore.md#uncommitted">uncommitted</a> across all   datastores that this virtual machine is located on. |
| unshared | long | None | None | Total storage space, in bytes, occupied by the virtual machine across   all datastores, that is not shared with any other virtual machine. |
| timestamp | datetime | None | None | Time when values in this structure were last updated. |


