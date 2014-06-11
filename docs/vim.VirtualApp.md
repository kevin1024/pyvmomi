vim.VirtualApp
==============
inherits from [vim.ResourcePool](vim.ResourcePool.md "vim.ResourcePool")
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Represents a multi-tiered software solution. A vApp is a collection of    virtual machines (and potentially other vApp containers) that are operated and    monitored as a unit. From a manage perspective, a multi-tiered vApp acts a    lot like a virtual machine object. It has power operations, networks, datastores,    and its resource usage can be configured.     <p>   From a technical perspective, a vApp container is a specialized resource pool that   has been extended with the following capabilities:   <li>   <ul>Product information such as product name, vendor, properties,        and licenses.</ul>   <ul>A power-on/power-off sequence specification</ul>   <ul>Support for import/export vApps as OVF packages</ul>   <ul>An OVF environment that allows for application-level customization</ul>   </li>    <p>   <b>Destroying a vApp</b>   <p>   When a vApp is destroyed, all of its virtual machines are destroyed,   as well as any child vApps.   <p>   The VApp.Delete privilege must be held on the vApp as well as the   parent folder of the vApp.  Also, the VApp.Delete privilege must   be held on any child vApps that would be destroyed by the operation.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='parentFolder'>parentFolder</a> | [vim.Folder](vim.Folder.md "vim.Folder") | true | System.View | A reference to the parent folder in the VM and Template folder hierarchy. This    is only set for a root vApp. A root vApp is a vApp that is not a child of   another vApp. |
| <a href='datastore'>datastore</a> | [vim.Datastore](vim.Datastore.md "vim.Datastore") | true | System.View | A collection of references to the subset of datastore objects used by this    vApp. |
| <a href='network'>network</a> | [vim.Network](vim.Network.md "vim.Network") | true | System.View | A collection of references to the subset of network objects that   is used by this virtual machine. |
| <a href='vAppConfig'>vAppConfig</a> | [vim.vApp.VAppConfigInfo](vim.vApp.VAppConfigInfo.md "vim.vApp.VAppConfigInfo") | true | System.Read | Configuration of this package. |
| <a href='parentVApp'>parentVApp</a> | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | true | None | Reference to the parent vApp. |
| <a href='childLink'>childLink</a> | [vim.VirtualApp.LinkInfo](vim.VirtualApp.LinkInfo.md "vim.VirtualApp.LinkInfo") | true | None | List of linked children. |


UpdateVAppConfig([spec](vim.vApp.VAppConfigSpec.md "vim.vApp.VAppConfigSpec"))
------------------------------------------------------------------------------
 raises [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.InvalidIndexArgument](vim.fault.InvalidIndexArgument.md "vim.fault.InvalidIndexArgument"), [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault")

---
| service name | UpdateVAppConfig |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | dynamic |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the vApp is busy. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | for bad configuration, such as invalid           property types. |
| [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess") | if another operation conflicted with this operation. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | vim.fault.FileFault |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | vim.fault.InvalidName |
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | vim.fault.DuplicateName |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | vim.fault.InvalidState |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | vim.fault.InsufficientResourcesFault |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | vim.fault.InvalidDatastore |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the reconfiguration is not possible given the            current powerState of the vApp. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | for wrong input. |
| [vim.fault.InvalidIndexArgument](vim.fault.InvalidIndexArgument.md "vim.fault.InvalidIndexArgument") | if a wrong key is used in one of the arrays. For           example, for duplicated entries in entityConfig. |




UpdateLinkedChildren([addChangeSet](vim.VirtualApp.LinkInfo.md "vim.VirtualApp.LinkInfo"), [removeSet](vim.ManagedEntity.md "vim.ManagedEntity"))
-------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
### Deprecated
As of vSphere API 5.1.

| service name | UpdateLinkedChildren |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#vim.version.version5) |
| privilege    | dynamic |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess") | If a concurrent modification happens while adding the link. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | See above description. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | If the target of the link is not in the same datacenter. |




CloneVApp([name](#string "string"), [target](vim.ResourcePool.md "vim.ResourcePool"), [spec](vim.vApp.CloneSpec.md "vim.vApp.CloneSpec"))
-----------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.MigrationFault](vim.fault.MigrationFault.md "vim.fault.MigrationFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault")

---
| service name | CloneVApp |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | VApp.Clone |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the           vApp's current state. For example, if the virtual machine           configuration information is not available, or if the vApp          is running. |
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if the operation cannot be performed on the          target datastores. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the vApp is busy. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if one of the virtual machines are not compatible with a          destination host. Typically, a specific subclass of this exception is          thrown, such as IDEDiskNotSupported. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there was an error accessing one of the virtual machine files. |
| [vim.fault.MigrationFault](vim.fault.MigrationFault.md "vim.fault.MigrationFault") | if it is not possible to migrate one of the virtual machines          to the destination. This is typically due to hosts being incompatible,          such as mismatch in network polices or access to networks and datastores.          Typically, a more specific subclass is thrown. |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | if this operation would violate a resource          usage policy. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the vApp is powered on. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the operation is not supported by the current agent. |




ExportVApp()
------------
 raises [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | ExportVApp |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | VApp.Export |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the vApp is powered on. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the vApp is busy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the           vApp's current state. For example, if the virtual machine           configuration information is not available, or if the vApp          is running. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there was an error accessing one of the virtual machine files. |




PowerOnVApp()
-------------
 raises [vmodl.fault.NotEnoughLicenses](vmodl.fault.NotEnoughLicenses.md "vmodl.fault.NotEnoughLicenses"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault"), [vim.fault.MissingNetworkIpConfig](vim.fault.MissingNetworkIpConfig.md "vim.fault.MissingNetworkIpConfig"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.VAppConfigFault](vim.fault.VAppConfigFault.md "vim.fault.VAppConfigFault"), [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault")

---
| service name | PowerOnVApp |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | VApp.PowerOn |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the vApp is busy |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if it fails to power on a virtual machine due to no host                availability, or unable to access the configuration file of a VM. |
| [vim.fault.InsufficientResourcesFault](vim.fault.InsufficientResourcesFault.md "vim.fault.InsufficientResourcesFault") | if this operation would violate a resource          usage policy. |
| [vim.fault.VmConfigFault](vim.fault.VmConfigFault.md "vim.fault.VmConfigFault") | if a configuration issue on the vApp or a virtual           machine in the vApp prevents the power-on to complete. Typically, a           more specific fault, such as InvalidPropertyType is thrown. |
| [vim.fault.VAppConfigFault](vim.fault.VAppConfigFault.md "vim.fault.VAppConfigFault") | if a configuration issue on a vApp prevents the           power-on. Typically, a more specific fault, MissingPowerOnConfiguration,          is thrown. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a problem accessing the virtual machine on the          filesystem. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the vApp is already running |
| [vmodl.fault.NotEnoughLicenses](vmodl.fault.NotEnoughLicenses.md "vmodl.fault.NotEnoughLicenses") | if there are not enough licenses to power on one or more                            virtual machines. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the vApp is marked as a template. |
| [vim.fault.MissingNetworkIpConfig](vim.fault.MissingNetworkIpConfig.md "vim.fault.MissingNetworkIpConfig") | if no network configuration exists for the primary           network for the vApp. |




PowerOffVApp()
--------------
 raises [vim.fault.VAppConfigFault](vim.fault.VAppConfigFault.md "vim.fault.VAppConfigFault"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.MissingPowerOffConfiguration](vim.fault.MissingPowerOffConfiguration.md "vim.fault.MissingPowerOffConfiguration"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | PowerOffVApp |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | VApp.PowerOff |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the vApp is busy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the          vApp's current state. For example, if the vApp is in the          process of being started. |
| [vim.fault.VAppConfigFault](vim.fault.VAppConfigFault.md "vim.fault.VAppConfigFault") | vim.fault.VAppConfigFault |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the vApp is not running |
| [vim.fault.MissingPowerOffConfiguration](vim.fault.MissingPowerOffConfiguration.md "vim.fault.MissingPowerOffConfiguration") | if no vApp powerOff configuration          has been specified. |




SuspendVApp()
-------------
 raises [vim.fault.VAppConfigFault](vim.fault.VAppConfigFault.md "vim.fault.VAppConfigFault"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | SuspendVApp |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#vim.version.version5) |
| privilege    | VApp.Suspend |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the vApp is busy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the          vApp's current state. For example, if the vApp is in the          process of being started. |
| [vim.fault.VAppConfigFault](vim.fault.VAppConfigFault.md "vim.fault.VAppConfigFault") | vim.fault.VAppConfigFault |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the vApp is not running |




unregisterVApp()
----------------
 raises [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | unregisterVApp |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | VApp.Unregister |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess") | vim.fault.ConcurrentAccess |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | vim.fault.InvalidState |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the vApp is running. |




