vim.OvfManager.CreateDescriptorParams
=====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Collection of parameters for createDescriptor

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ovfFiles | [vim.OvfManager.OvfFile](vim.OvfManager.OvfFile.md "vim.OvfManager.OvfFile") | true | None | Contains information about the files of the entity, if they have already been  downloaded. Needed to construct the References section of the descriptor.  <p>  OvfFile is a positive list of files to include in the export. An Empty list  will do no filtering. |
| name | string | true | None | The ovf:id to use for the top-level OVF Entity. If unset, the entity's  product name is used if available. Otherwise, the VI entity name is used. |
| description | string | true | None | The contents of the Annontation section of the top-level OVF Entity. If unset,  any existing annotation on the entity is left unchanged. |
| includeImageFiles | bool | true | None | Controls whether attached image files should be included in the descriptor.  This applies to image files attached to VirtualCdrom and VirtualFloppy. |
| exportOption | string | true | None | An optional argument for modifying the export process.  The option is used to control what extra information that will be included in the  OVF descriptor.  <p>  To get a list of supported keywords see <a href="vim.OvfManager.md#ovfExportOption">ovfExportOption</a>. Unknown  options will be ignored by the server. |
| snapshot | [vim.vm.Snapshot](vim.vm.Snapshot.md "vim.vm.Snapshot") | true | None | Snapshot reference from which the OVF descriptor should be based.  <p>  If this parameter is set, the OVF descriptor is based off the  snapshot point. This means that the OVF descriptor will have the  same configuration as the virtual machine at the time the snapshot  was taken.  <p>  The snapshot must be belong to the specified ManagedEntity in the  createDescriptor call. |


