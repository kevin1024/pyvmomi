vim.ImportSpec
==============
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


An ImportSpec is used when importing VMs or vApps.   <p>  It can be built from scratch, or it can be generated from an OVF descriptor using the  service interface <a href="vim.OvfManager.md">OvfManager</a>.  <p>  This class is the abstract base for <a href="vim.vm.VmImportSpec.md">VirtualMachineImportSpec</a> and  <a href="vim.vApp.VAppImportSpec.md">VirtualAppImportSpec</a>.  These three classes form a composite structure  that allows us to contain arbitrarily complex entitites in a single ImportSpec.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entityConfig | [vim.vApp.EntityConfigInfo](vim.vApp.EntityConfigInfo.md "vim.vApp.EntityConfigInfo") | true | None | Configuration of sub-entities (virtual machine or vApp). This is used for  sub-entities of a vApp that could be a virtual machine or a vApp. |
| instantiationOst | [vim.OvfConsumer.OstNode](vim.OvfConsumer.OstNode.md "vim.OvfConsumer.OstNode") | true | None | The instantiation OST (see <a href="vim.OvfConsumer.md">OvfConsumer</a> ) to be consumed by OVF  consumers. |


