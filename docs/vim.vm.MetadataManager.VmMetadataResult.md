vim.vm.MetadataManager.VmMetadataResult
=======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


A list of VmMetadataResults are returned for successful and  non-successful results of an update or retrieve operation.<br>See MetadataManager#updateMetadata(VmMetadataOwner,See MetadataManager#retrieveMetadata(VmMetadataOwner,See MetadataManager#retrieveAllMetadata(VmMetadataOwner,See MetadataManager#clearMetadata(VmMetadataOwner,

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vmMetadata | [vim.vm.MetadataManager.VmMetadata](vim.vm.MetadataManager.VmMetadata.md "vim.vm.MetadataManager.VmMetadata") | None | None | The VM-specific metadata |
| error | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | MethodFault set for errors in getting or setting  the VmMetadata. |


