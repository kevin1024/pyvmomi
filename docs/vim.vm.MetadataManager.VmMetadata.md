vim.vm.MetadataManager.VmMetadata
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


VmMetadata is a pair of VM ID and opaque metadata.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vmId | string | None | None | Datastore URL-based ID for VM, for example,  "[datastore1] SomeVM/SomeVM.vmx". |
| metadata | string | true | None | Opaque metadata for the VM identified by vmId. If no  value is supplied, the entry for this VM is removed. |


