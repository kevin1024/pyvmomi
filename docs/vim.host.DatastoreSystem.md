vim.host.DatastoreSystem
========================


This managed object creates and removes datastores from the host.   <p>   To a host, a datastore is a storage abstraction that is backed by one   of several types of storage volumes:   <dl>   <dt><b>Local file system</b></dt>   <dd>   A datastore that is backed by a local file system volume uses a host native   local file system such as NTFS or ext3.  The datastore is created by   identifying a file path for a directory in which virtual machine data will   be stored.  When the datastore is deleted, the mapping from the datastore to   the file is deleted.  The contents of the directory are not deleted.   </dd>   <p>   <dt><b>NAS Volume</b></dt>   <dd>   A datastore that is backed by a network-attached storage device is created   by specifying the required data needed to attach the volume to the host.   Destroying the datastore detaches the volume from the host.   </dd>   <p>   <dt><b>VMFS</b></dt>   <dd>   A datastore that is backed by a VMware File System (VMFS) is created by   specifying a disk with unpartitioned space, the desired disk partition   format on the disk, and some VMFS attributes.   <p>   An ESX Server system automatically discovers the VMFS volume on attached Logical   Unit Numbers (LUNs) on startup and after re-scanning the host bus adapter.   Datastores are automatically created.  The datastore label is based on the   VMFS volume label.  If there is a conflict with an existing datastore,   it is made unique by appending a suffix.  The VMFS volume label will   be unchanged.   <p>   Destroying the datastore removes the partitions that compose the VMFS volume.   </dd>   </dl>   Datastores are never automatically removed because transient storage   connection outages may occur.  They must be removed from the host using   this interface.<br>See <a href="vim.Datastore.md">Datastore</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='datastore'>datastore</a> | [vim.Datastore](vim.Datastore.md "vim.Datastore") | true | System.View | List of datastores on this host. |
| <a href='capabilities'>capabilities</a> | [vim.host.DatastoreSystem.Capabilities](vim.host.DatastoreSystem.Capabilities.md "vim.host.DatastoreSystem.Capabilities") | None | None | Capability vector indicating the available product features. |


UpdateLocalSwapDatastore([datastore](vim.Datastore.md "vim.Datastore"))
-----------------------------------------------------------------------
 raises [vim.fault.InaccessibleDatastore](vim.fault.InaccessibleDatastore.md "vim.fault.InaccessibleDatastore"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.DatastoreNotWritableOnHost](vim.fault.DatastoreNotWritableOnHost.md "vim.fault.DatastoreNotWritableOnHost")

---
| service name | UpdateLocalSwapDatastore |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InaccessibleDatastore](vim.fault.InaccessibleDatastore.md "vim.fault.InaccessibleDatastore") | if the datastore argument is set and   the host cannot access the indicated datastore. |
| [vim.fault.DatastoreNotWritableOnHost](vim.fault.DatastoreNotWritableOnHost.md "vim.fault.DatastoreNotWritableOnHost") | if the datastore argument is set and   the host cannot write to the indicated datastore. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the datastore argument is set and the   <a href="vim.host.Capability.md#localSwapDatastoreSupported">localSwapDatastoreSupported</a>   capability is not true for the host. |




QueryAvailableDisksForVmfs([datastore](vim.Datastore.md "vim.Datastore"))
-------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | QueryAvailableDisksForVmfs |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the named VMFS datastore is not found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if unable to query disk information. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if named VMFS datastore is not a VMFS datastore. |




QueryVmfsDatastoreCreateOptions([devicePath](#string "string"))
---------------------------------------------------------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | QueryVmfsDatastoreCreateOptions |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the device is not found.<br>See <a href="vim.host.ScsiDisk.md#devicePath">devicePath</a><br> |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if unable to get the current partition information for           the device.<br>See <a href="vim.host.ScsiDisk.md#devicePath">devicePath</a><br> |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server.<br>See <a href="vim.host.ScsiDisk.md#devicePath">devicePath</a><br> |




CreateVmfsDatastore([spec](vim.host.VmfsDatastoreCreateSpec.md "vim.host.VmfsDatastoreCreateSpec"))
---------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | CreateVmfsDatastore |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if a datastore with the same name already exists. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if unable to format the VMFS volume or           gather information about the created volume. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the datastore name is invalid, or the spec           is invalid. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server system. |




QueryVmfsDatastoreExtendOptions([datastore](vim.Datastore.md "vim.Datastore"), [devicePath](#string "string"))
--------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | QueryVmfsDatastoreExtendOptions |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if a datastore or device with the given name could not be found                or if the datastore is unmounted.<br>See <a href="vim.host.ScsiDisk.md#devicePath">devicePath</a><br> |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if unable to get the current partition information for           the device.<br>See <a href="vim.host.ScsiDisk.md#devicePath">devicePath</a><br> |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server.<br>See <a href="vim.host.ScsiDisk.md#devicePath">devicePath</a><br> |




QueryVmfsDatastoreExpandOptions([datastore](vim.Datastore.md "vim.Datastore"))
------------------------------------------------------------------------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | QueryVmfsDatastoreExpandOptions |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the specified datastore could not be found or is unmounted. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if unable to get partition information for the           devices on which the extents reside |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server. |




ExtendVmfsDatastore([datastore](vim.Datastore.md "vim.Datastore"), [spec](vim.host.VmfsDatastoreExtendSpec.md "vim.host.VmfsDatastoreExtendSpec"))
--------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | ExtendVmfsDatastore |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if a datastore with the name could not be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if unable to extend the VMFS volume. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server. |




ExpandVmfsDatastore([datastore](vim.Datastore.md "vim.Datastore"), [spec](vim.host.VmfsDatastoreExpandSpec.md "vim.host.VmfsDatastoreExpandSpec"))
--------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | ExpandVmfsDatastore |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if a datastore with the name could not be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if unable to expand the VMFS volume. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server. |




CreateNasDatastore([spec](vim.host.NasVolume.Specification.md "vim.host.NasVolume.Specification"))
--------------------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.NoGateway](vim.fault.NoGateway.md "vim.fault.NoGateway"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vim.fault.NoVirtualNic](vim.fault.NoVirtualNic.md "vim.fault.NoVirtualNic")

---
| service name | CreateNasDatastore |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if a datastore with the same name already exists. |
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | if the local path already exists on the host, or           the remote path is already mounted on the host. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if unable to mount the NAS volume. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the datastore name is invalid, or the spec           is invalid. |
| [vim.fault.NoVirtualNic](vim.fault.NoVirtualNic.md "vim.fault.NoVirtualNic") | if VMkernel TCPIP stack is not configured. |
| [vim.fault.NoGateway](vim.fault.NoGateway.md "vim.fault.NoGateway") | if VMkernel gateway is not configured. |




CreateLocalDatastore([name](#string "string"), [path](#string "string"))
------------------------------------------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | CreateLocalDatastore |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if a datastore with the same name already exists. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if unable to create the datastore on host. |
| [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound") | if path doesn't exist |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if name is not valid datastore name |




RemoveDatastore([datastore](vim.Datastore.md "vim.Datastore"))
--------------------------------------------------------------
 raises [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | RemoveDatastore |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the datastore could not be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if unable to umount the NAS volume for NAS           datastore, or gather the existing volume information. |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | for a VMFS volume if there is any VM registered           on any host attached to this datastore. |




ConfigureDatastorePrincipal([userName](#string "string"), [password](#string "string"))
---------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | ConfigureDatastorePrincipal |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Maintenance |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the host is not in maintenance mode. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if unable to configure the datastore principal. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if userName or password is not valid. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if this feature is not supported on the host. |




QueryUnresolvedVmfsVolumes()
----------------------------

| service name | QueryUnresolvedVmfsVolumes |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




ResignatureUnresolvedVmfsVolume([resolutionSpec](vim.host.UnresolvedVmfsResignatureSpec.md "vim.host.UnresolvedVmfsResignatureSpec"))
-------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.VmfsAmbiguousMount](vim.fault.VmfsAmbiguousMount.md "vim.fault.VmfsAmbiguousMount"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | ResignatureUnresolvedVmfsVolume |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.VmfsAmbiguousMount](vim.fault.VmfsAmbiguousMount.md "vim.fault.VmfsAmbiguousMount") | when ESX is unable to resolve the extents           of a VMFS volume unambiguously. This is thrown only when           a VMFS volume has multiple extents and multiple copies of           non-head extents are detected, and the user has not           specified one copy of every extent. Please note that some           versions of ESX may not support resolving the situation           where multiple copies of non-head extents are detected,           even if one copy of every extent is specified in the           method parameter. To resolve such a situation, the user           is expected to change the configuration (for example,           using array management tools) so that only one copy of           each non-head extent is presented to ESX. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |




