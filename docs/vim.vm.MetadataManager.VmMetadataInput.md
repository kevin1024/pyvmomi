vim.vm.MetadataManager.VmMetadataInput
======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


VmMetadataInput specifies the operation and metadata for a  specific VM.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| operation | string | None | None | The input operation type.  The values come from VmMetadataOp |
| vmMetadata | [vim.vm.MetadataManager.VmMetadata](vim.vm.MetadataManager.VmMetadata.md "vim.vm.MetadataManager.VmMetadata") | None | None | the VM and optional metadata |


