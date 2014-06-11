vim.vm.check.ProvisioningChecker
================================
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


A singleton managed object that can answer questions about    the feasibility of certain provisioning operations.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


QueryVMotionCompatibilityEx([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [host](vim.HostSystem.md "vim.HostSystem"))
-------------------------------------------------------------------------------------------------------------------------

| service name | QueryVMotionCompatibilityEx |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|




CheckMigrate([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [host](vim.HostSystem.md "vim.HostSystem"), [pool](vim.ResourcePool.md "vim.ResourcePool"), [state](vim.VirtualMachine.PowerState.md "vim.VirtualMachine.PowerState"), [testType](#string "string"))
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | CheckMigrate |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | vim.fault.InvalidState |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the target host(s) and target pool for a          migration are not associated with the same compute resource,          or if the host parameter is left unset when the target pool is          associated with a non-DRS cluster. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the state argument is set and at least one          of the specified virtual machines is not in that power state. |




CheckRelocate([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [spec](vim.vm.RelocateSpec.md "vim.vm.RelocateSpec"), [testType](#string "string"))
---------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | CheckRelocate |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the           host or virtual machine's current state. For example, if the host is in          maintenance mode, or if the virtual machine's configuration information          is not available. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the virtual machine is marked as a template. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | in the following cases:  <ul>     <li>  the target host and target pool are not associated with the           same compute resource</li>     <li>  the target pool represents a cluster without DRS enabled,           and the host is not specified</li>     <li>  Datastore in a diskLocator entry is not specified</li>     <li>  the specified device ID cannot be found in the virtual machine's current           configuration  </li>     <li>  the object specified in relocate cannot be found</li>  </ul> |




