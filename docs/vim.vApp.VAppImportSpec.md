vim.vApp.VAppImportSpec
=======================
inherits from [vim.ImportSpec](docs/vim.ImportSpec.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


A VAppImportSpec is used by <a href="vim.ResourcePool.md#importVApp">ResourcePool.importVApp</a> when importing vApps (single VM or multi-VM).  <p>  It provides all information needed to import a <a href="vim.VirtualApp.md">VirtualApp</a>.  <p>  See also <a href="vim.ImportSpec.md">ImportSpec</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | The name of the vApp |
| vAppConfigSpec | [vim.vApp.VAppConfigSpec](vim.vApp.VAppConfigSpec.md "vim.vApp.VAppConfigSpec") | None | None | vApp configuration |
| resourcePoolSpec | [vim.ResourceConfigSpec](vim.ResourceConfigSpec.md "vim.ResourceConfigSpec") | None | None | Resource pool specification.  <p>  If resourcePoolSpec.entity is specified, that resource pool is used as the parent  resource pool and the vApp will be made a linked child to the parent vApp. This  field is ignored for the root node in an ImportSpec tree.   Use of resourcePoolSpec.entity for creating linked children is deprecated as of  vSphere API 5.1. |
| child | [vim.ImportSpec](vim.ImportSpec.md "vim.ImportSpec") | true | None | Contains a list of children (<a href="vim.VirtualMachine.md">VirtualMachine</a>s and  <a href="vim.VirtualApp.md">VirtualApp</a>s). |


