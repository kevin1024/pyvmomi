vim.dvs.VmwareDistributedVirtualSwitch
======================================
inherits from [vim.DistributedVirtualSwitch](vim.DistributedVirtualSwitch.md "vim.DistributedVirtualSwitch")
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.dvs.VmwareDistributedVirtualSwitch.md">VmwareDistributedVirtualSwitch</a> managed object  is the VMware implementation of a distributed virtual switch.  The functionality listed here is for a VMware distributed virtual switch only.  <p>  When you use a VMware distributed virtual switch, you can perform  backup and restore operations on the VMware switch. You can also  perform rollback operations on the switch and on portgroups  associated with the VMware switch. See the description for the  following methods:  <ul>  <li><a href="vim.dvs.DistributedVirtualSwitchManager.md#exportEntity">DVSManagerExportEntity_Task</a></li>  <li><a href="vim.dvs.DistributedVirtualSwitchManager.md#importEntity">DVSManagerImportEntity_Task</a></li>  <li><a href="vim.DistributedVirtualSwitch.md#rollback">DVSRollback_Task</a></li>  <li><a href="vim.dvs.DistributedVirtualPortgroup.md#rollback">DVPortgroupRollback_Task</a></li>  </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


UpdateDVSLacpGroupConfig([lacpGroupSpec](vim.dvs.VmwareDistributedVirtualSwitch.LacpGroupSpec.md "vim.dvs.VmwareDistributedVirtualSwitch.LacpGroupSpec"))
---------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | UpdateDVSLacpGroupConfig |
|:--|:--|
| since version | [vSphere API 5.5](vim.version.md#vim.version.version5) |
| privilege    | DVSwitch.Modify |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | if operation fails on any host or if there are other update failures. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if multiple Link Aggregation Control Protocol   is not supported on the switch. |




