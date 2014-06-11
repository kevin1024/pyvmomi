vim.OvfManager.CreateImportSpecResult
=====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The CreateImportSpecResult contains all information regarding the import that can  be extracted from the OVF descriptor.  <p>  For example, this includes the list of items that the caller must upload in order  to complete the import, but not the list of URLs to which the files must be  uploaded. These paths are not known until the VMs have been created, ie. until  <a href="vim.ResourcePool.md#importVApp">ResourcePool.importVApp</a> has been  called.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| importSpec | [vim.ImportSpec](vim.ImportSpec.md "vim.ImportSpec") | true | None | The ImportSpec contains information about which <a href="vim.VirtualMachine.md">VirtualMachine</a>s  and <a href="vim.VirtualApp.md">VirtualApp</a>s are present in the entity and  how they relate to each other. |
| fileItem | [vim.OvfManager.FileItem](vim.OvfManager.FileItem.md "vim.OvfManager.FileItem") | true | None | The files that must be uploaded by the caller as part of importing the entity.  <p>  The files must be uploaded in order, because some of them may be delta files  that patch already-uploaded files. |
| warning | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | Non-fatal warnings from the processing.  The ImportSpec will be valid, but the  user may choose to reject it based on these warnings. |
| error | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | Errors that happened during processing. Something will be wrong with the  ImportSpec, or it is not present. |


