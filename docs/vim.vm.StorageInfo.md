vim.vm.StorageInfo
==================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Information about the amount of storage used by a virtual machine across   datastores that it is located on.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| perDatastoreUsage | [vim.vm.StorageInfo.UsageOnDatastore](vim.vm.StorageInfo.UsageOnDatastore.md "vim.vm.StorageInfo.UsageOnDatastore") | true | None | Storage space used by this virtual machine on all datastores that it   is located on.   <p>   Total storage space committed to this virtual machine across all datastores is   simply an aggregate of the property   <a href="vim.vm.StorageInfo.UsageOnDatastore.md#committed">committed</a>.<br>See <a href="vim.vm.Summary.StorageSummary.md#committed">committed</a><br> |
| timestamp | datetime | None | None | Time when values in this structure were last updated. |


