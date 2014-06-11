vim.OvfManager
==============
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Service interface to parse and generate OVF descriptors.  <p>  The purpose of this interface is to make it easier for callers to import VMs and  vApps from OVF packages and to export VI packages to OVF. In the following  description, the term "client" is used to mean any caller of the interface.  <p>  This interface only converts between OVF and VI types. To actually import and export  entities, use <a href="vim.ResourcePool.md#importVApp">ResourcePool.importVApp</a>,  <a href="vim.VirtualMachine.md#exportVm">VirtualMachine.exportVm</a> and  <a href="vim.VirtualApp.md#exportVApp">VirtualApp.exportVApp</a>.   <h2>Import</h2>  For the import scenario, the typical sequence of events is as follows:  <p>  The client calls parseDescriptor to obtain information about the OVF descriptor. This  typically includes information (such as a list of networks) that must be mapped to VI  infrastructure entities.  <p>  The OVF descriptor is validated against the OVF Specification, and any errors or  warnings are returned as part of the ParseResult. For example, the parser might  encounter a section marked required that it does not understand, or the XML descriptor  might be malformed.  <p>  The client decides on network mappings, datastore, properties etc. It then calls  createImportSpec to obtain the parameters needed to call  <a href="vim.ResourcePool.md#importVApp">ResourcePool.importVApp</a>.  <p>  If any warnings are present, the client will review these and decide whether to  proceed or not. If errors are present, the ImportSpec will be missing, so  the client is forced to give up or fix the problems and then try again.  <p>  The client now calls <a href="vim.ResourcePool.md#importVApp">ResourcePool.importVApp</a>, passing the ImportSpec as a parameter. This will create  the virtual machines and <a href="vim.VirtualApp.md">VirtualApp</a> objects in VI and return locations  to which the files of the entity can be uploaded. It also returns a lease that  controls the duration of the lock taken on the newly created inventory objects. When  all files have been uploaded, the client must release this lease.   <h2>Export</h2>  Creating the OVF descriptor is the last part of exporting an entity to OVF. At this  point, the client has already downloaded all files for the entity, optionally  compressing and/or chunking them (however, the client may do a "dry run" of creating  the descriptor before downloading the files. See <a href="vim.OvfManager.md#createDescriptor">OvfManager.createDescriptor</a>).  <p>  In addition to the entity reference itself, information about the choices made on  these files is passed to createDescriptor as a list of OvfFile instances.  <p>  The client must inspect and act upon warnings and errors as previously described.  <p>  No matter if the export succeeds or fails, the client is responsible for releasing the  shared state lock taken on the entity (by <a href="vim.VirtualMachine.md#exportVm">VirtualMaching.exportVm</a> or <a href="vim.VirtualApp.md#exportVApp">VirtualApp.exportVApp</a>) during the export.   <h2>Error handling</h2>  All result types contain warning and error lists. Warnings do not cause processing to  fail, but the caller (typically, the user of a GUI client) may choose to reject the  result based on the warnings issued.  <p>  Errors cause processing to abort by definition.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='ovfImportOption'>ovfImportOption</a> | [vim.OvfManager.OvfOptionInfo](vim.OvfManager.OvfOptionInfo.md "vim.OvfManager.OvfOptionInfo") | true | System.View | Returns an array of <a href="vim.OvfManager.OvfOptionInfo.md">OvfOptionInfo</a> object that specifies what options the server  support for modifing/relaxing the OVF import process.  <p> |
| <a href='ovfExportOption'>ovfExportOption</a> | [vim.OvfManager.OvfOptionInfo](vim.OvfManager.OvfOptionInfo.md "vim.OvfManager.OvfOptionInfo") | true | System.View | Returns an array of <a href="vim.OvfManager.OvfOptionInfo.md">OvfOptionInfo</a> object that specifies what options the server  support for exporting an OVF descriptor.  <p> |


ValidateHost([ovfDescriptor](#string "string"), [host](vim.HostSystem.md "vim.HostSystem"), [vhp](vim.OvfManager.ValidateHostParams.md "vim.OvfManager.ValidateHostParams"))
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | ValidateHost |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if a required managed entity is busy. |
| [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess") | if a concurrency issue prevents the operation from          succeeding. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a generic file error |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation failed due to the current state of the system. |




ParseDescriptor([ovfDescriptor](#string "string"), [pdp](vim.OvfManager.ParseDescriptorParams.md "vim.OvfManager.ParseDescriptorParams"))
-----------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | ParseDescriptor |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if a required managed entity is busy. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if a configuration issue prevents the operation from          succeeding. Typically, a more specific subclass is thrown. |
| [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess") | if a concurrency issue prevents the operation from          succeeding. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a generic file error |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation failed due to the current state of the system. |




CreateImportSpec([ovfDescriptor](#string "string"), [resourcePool](vim.ResourcePool.md "vim.ResourcePool"), [datastore](vim.Datastore.md "vim.Datastore"), [cisp](vim.OvfManager.CreateImportSpecParams.md "vim.OvfManager.CreateImportSpecParams"))
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault")

---
| service name | CreateImportSpec |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if a required managed entity is busy. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if a configuration issue prevents the operation from          succeeding. Typically, a more specific subclass is thrown. |
| [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess") | if a concurrency issue prevents the operation from          succeeding. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a generic file error |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation failed due to the current state of the system. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | vim.fault.InvalidDatastore |




CreateDescriptor([obj](vim.ManagedEntity.md "vim.ManagedEntity"), [cdp](vim.OvfManager.CreateDescriptorParams.md "vim.OvfManager.CreateDescriptorParams"))
----------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | CreateDescriptor |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if a required managed entity is busy. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if a configuration issue prevents the operation from          succeeding. Typically, a more specific subclass is thrown. |
| [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess") | if a concurrency issue prevents the operation from          succeeding. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a generic file error |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation failed due to the current state of the system. |




