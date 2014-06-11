vim.dvs.DistributedVirtualSwitchManager
=======================================
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.dvs.DistributedVirtualSwitchManager.md">DistributedVirtualSwitchManager</a> provides methods  that support the following operations:  <ul>  <li>Backup and restore operations for <a href="vim.dvs.VmwareDistributedVirtualSwitch.md">VmwareDistributedVirtualSwitch</a>  and associated <a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a> managed objects.</li>  <li>Query operations for information about portgroups and distributed  virtual switches.</li>  <li>Distributed virtual switch configuration update operations.  </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


QueryAvailableDvsSpec()
-----------------------

| service name | QueryAvailableDvsSpec |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




QueryCompatibleHostForNewDvs([container](vim.ManagedEntity.md "vim.ManagedEntity"), [switchProductSpec](vim.dvs.ProductSpec.md "vim.dvs.ProductSpec"))
------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | QueryCompatibleHostForNewDvs |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If the productSpec value is not valid or                            recognized. |




QueryCompatibleHostForExistingDvs([container](vim.ManagedEntity.md "vim.ManagedEntity"), [dvs](vim.DistributedVirtualSwitch.md "vim.DistributedVirtualSwitch"))
---------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | QueryCompatibleHostForExistingDvs |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If the switch value is not valid or                            recognized. |




QueryDvsCompatibleHostSpec([switchProductSpec](vim.dvs.ProductSpec.md "vim.dvs.ProductSpec"))
---------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | QueryDvsCompatibleHostSpec |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If the switchProductSpec value is not valid or                            recognized. |




QueryDvsFeatureCapability([switchProductSpec](vim.dvs.ProductSpec.md "vim.dvs.ProductSpec"))
--------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | QueryDvsFeatureCapability |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If the switchProductSpec value is not valid or                            recognized. |




QueryDvsByUuid([uuid](#string "string"))
----------------------------------------
 raises [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | QueryDvsByUuid |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | If a switch with the UUID doesn't exist. |




QueryDvsConfigTarget([host](vim.HostSystem.md "vim.HostSystem"), [dvs](vim.DistributedVirtualSwitch.md "vim.DistributedVirtualSwitch"))
---------------------------------------------------------------------------------------------------------------------------------------

| service name | QueryDvsConfigTarget |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




QueryDvsCheckCompatibility([hostContainer](vim.dvs.DistributedVirtualSwitchManager.HostContainer.md "vim.dvs.DistributedVirtualSwitchManager.HostContainer"), [dvsProductSpec](vim.dvs.DistributedVirtualSwitchManager.DvsProductSpec.md "vim.dvs.DistributedVirtualSwitchManager.DvsProductSpec"), [hostFilterSpec](vim.dvs.DistributedVirtualSwitchManager.HostDvsFilterSpec.md "vim.dvs.DistributedVirtualSwitchManager.HostDvsFilterSpec"))
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | QueryDvsCheckCompatibility |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If the dvsProductSpec value is not valid or                            recognized. |




RectifyDvsOnHost([hosts](vim.HostSystem.md "vim.HostSystem"))
-------------------------------------------------------------
 raises [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault")

---
| service name | RectifyDvsOnHost |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#vim.version.version5) |
| privilege    | System.Read |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | if operation fails on any host or if there are other update failures. |




DVSManagerExportEntity([selectionSet](vim.SelectionSet.md "vim.SelectionSet"))
------------------------------------------------------------------------------
 raises [vim.fault.BackupBlobWriteFailure](vim.fault.BackupBlobWriteFailure.md "vim.fault.BackupBlobWriteFailure"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | DVSManagerExportEntity |
|:--|:--|
| since version | [vSphere API 5.1](vim.version.md#vim.version.version5) |
| privilege    | dynamic |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | If entity in selectionSet doesn't exist. |
| [vim.fault.BackupBlobWriteFailure](vim.fault.BackupBlobWriteFailure.md "vim.fault.BackupBlobWriteFailure") | if failed to create backup config blob. |




DVSManagerImportEntity([entityBackup](vim.dvs.EntityBackup.Config.md "vim.dvs.EntityBackup.Config"), [importType](#string "string"))
------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | DVSManagerImportEntity |
|:--|:--|
| since version | [vSphere API 5.1](vim.version.md#vim.version.version5) |
| privilege    | dynamic |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | if operation fails on any host. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | If entity in <a href="vim.dvs.EntityBackup.Config.md#key">key</a> doesn't exist. |




DVSManagerLookupDvPortGroup([switchUuid](#string "string"), [portgroupKey](#string "string"))
---------------------------------------------------------------------------------------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | DVSManagerLookupDvPortGroup |
|:--|:--|
| since version | [vSphere API 5.1](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | If the portgroup for the specified inputs was not found. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | If the operation is not supported. |




