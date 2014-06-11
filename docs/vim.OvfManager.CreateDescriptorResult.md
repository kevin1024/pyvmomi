vim.OvfManager.CreateDescriptorResult
=====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The result of creating the OVF descriptor for the entity.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ovfDescriptor | string | None | None | The OVF descriptor for the entity. |
| error | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | Errors that happened during processing.  <p>  For example, unknown or unsupported devices could be found (in which case  this array will contain one or more instances of Unsupported-/UnknownDevice). |
| warning | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | Non-fatal warnings from the processing.  <p>  The result will be valid, but the user may choose to reject it based on these  warnings. |
| includeImageFiles | bool | true | None | Returns true if there are ISO or Floppy images attached to one or more VMs. |


