vim.vm.check.CompatibilityChecker
=================================
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


A singleton managed object that can answer questions about compatibility   of a virtual machine with a host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


CheckCompatibility([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [host](vim.HostSystem.md "vim.HostSystem"), [pool](vim.ResourcePool.md "vim.ResourcePool"), [testType](#string "string"))
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.NoActiveHostInCluster](vim.fault.NoActiveHostInCluster.md "vim.fault.NoActiveHostInCluster"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | CheckCompatibility |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | vim.fault.InvalidState |
| [vim.fault.NoActiveHostInCluster](vim.fault.NoActiveHostInCluster.md "vim.fault.NoActiveHostInCluster") | vim.fault.NoActiveHostInCluster |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the desired host and pool are not associated           with the same compute resource, or if the host parameter is left           unset when the specified pool is ssociated with a non-DRS cluster. |




