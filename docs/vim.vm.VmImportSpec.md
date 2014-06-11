vim.vm.VmImportSpec
===================
inherits from [vim.ImportSpec](docs/vim.ImportSpec.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


A VmImportSpec is used by <a href="vim.ResourcePool.md#importVApp">ResourcePool.importVApp</a> when importing entities.  <p>  It provides all information needed to import a <a href="vim.VirtualMachine.md">VirtualMachine</a>. So far,  this coincides with <a href="vim.vm.ConfigSpec.md">VirtualMachineConfigSpec</a>.   <p>  A VmImportSpec can be contained in a <a href="vim.vApp.VAppImportSpec.md">VirtualAppImportSpec</a> as part of  the ImportSpec for an entity.  <p>  See also <a href="vim.ImportSpec.md">ImportSpec</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| configSpec | [vim.vm.ConfigSpec](vim.vm.ConfigSpec.md "vim.vm.ConfigSpec") | None | None | Configuration for the virtual machine. |
| resPoolEntity | [vim.ResourcePool](vim.ResourcePool.md "vim.ResourcePool") | true | None | If specified, this resource pool will be used as the parent resource pool and the   virtual machine will be made a linked child to the parent vApp. This field is ignored   for the root node in an ImportSpec tree. |


