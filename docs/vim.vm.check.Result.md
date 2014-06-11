vim.vm.check.Result
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The result of a call to any of the methods in either   <a href="vim.vm.check.CompatibilityChecker.md">VirtualMachineCompatibilityChecker</a> or <a href="vim.vm.check.ProvisioningChecker.md">VirtualMachineProvisioningChecker</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vm | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | true | None | The virtual machine involved in the testing. |
| host | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | true | None | The host involved in the testing. |
| warning | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | A list of faults representing problems which may   require attention, but which are not fatal. |
| error | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | A list of faults representing problems which are fatal  to the operation.    For <a href="vim.vm.check.ProvisioningChecker.md">VirtualMachineProvisioningChecker</a> an error means that the   given provisioning operation would fail.   For <a href="vim.vm.check.CompatibilityChecker.md">VirtualMachineCompatibilityChecker</a> an error means that either  a power-on of this virtual machine would fail, or that the   virtual machine would not run correctly once powered-on. |


