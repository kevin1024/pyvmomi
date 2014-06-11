vim.host.StorageSystem
======================
inherits from [vim.ExtensibleManagedObject](vim.ExtensibleManagedObject.md "vim.ExtensibleManagedObject")


This managed object gets and sets configuration information   about the host's storage subsystem.  The properties and operations are   used to configure the host to make storage available for virtual machines.    This object contains properties that are specific to ESX Server and   general to both the ESX Server system and the hosted architecture.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='storageDeviceInfo'>storageDeviceInfo</a> | [vim.host.StorageDeviceInfo](vim.host.StorageDeviceInfo.md "vim.host.StorageDeviceInfo") | true | None | Host storage information up to the device level. |
| <a href='fileSystemVolumeInfo'>fileSystemVolumeInfo</a> | [vim.host.FileSystemVolumeInfo](vim.host.FileSystemVolumeInfo.md "vim.host.FileSystemVolumeInfo") | None | None | File system volume information for the host.  See the   <a href="vim.host.FileSystemVolumeInfo.md">FileSystemVolumeInfo</a> data   object type for more information. |
| <a href='systemFile'>systemFile</a> | string | true | None | Datastore paths of files used by the host system on   mounted volumes, for instance, the COS vmdk file of the   host. For information on datastore paths, see <a href="vim.Datastore.md">Datastore</a>. |
| <a href='multipathStateInfo'>multipathStateInfo</a> | [vim.host.MultipathStateInfo](vim.host.MultipathStateInfo.md "vim.host.MultipathStateInfo") | true | None | Runtime information about the state of a multipath path.   A null value will be returned if path state information is not available   for this system.   <p>   In systems prior to the plug-store architecture, the state of a path   may be accessible on the <a href="vim.host.MultipathInfo.md">HostMultipathInfo</a> data object   of the <a href="vim.host.StorageSystem.md#storageDeviceInfo">storageDeviceInfo</a> property. |


RetrieveDiskPartitionInfo([devicePath](#string "string"))
---------------------------------------------------------

| service name | RetrieveDiskPartitionInfo |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




ComputeDiskPartitionInfo([devicePath](#string "string"), [layout](vim.host.DiskPartitionInfo.Layout.md "vim.host.DiskPartitionInfo.Layout"), [partitionFormat](#string "string"))
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | ComputeDiskPartitionInfo |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the device could not be found.<br>See <a href="vim.host.DiskPartitionInfo.PartitionFormat.md">HostDiskPartitionInfoPartitionFormat</a><br> |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if unable to get the current partition information for           the device.<br>See <a href="vim.host.DiskPartitionInfo.PartitionFormat.md">HostDiskPartitionInfoPartitionFormat</a><br> |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the layout is invalid.<br>See <a href="vim.host.DiskPartitionInfo.PartitionFormat.md">HostDiskPartitionInfoPartitionFormat</a><br> |




ComputeDiskPartitionInfoForResize([partition](vim.host.ScsiDisk.Partition.md "vim.host.ScsiDisk.Partition"), [blockRange](vim.host.DiskPartitionInfo.BlockRange.md "vim.host.DiskPartitionInfo.BlockRange"), [partitionFormat](#string "string"))
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | ComputeDiskPartitionInfoForResize |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the device could not be found.<br>See <a href="vim.host.DiskPartitionInfo.PartitionFormat.md">HostDiskPartitionInfoPartitionFormat</a><br> |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if unable to get the current partition           information for the device.<br>See <a href="vim.host.DiskPartitionInfo.PartitionFormat.md">HostDiskPartitionInfoPartitionFormat</a><br> |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if blockRange or partition is invalid.<br>See <a href="vim.host.DiskPartitionInfo.PartitionFormat.md">HostDiskPartitionInfoPartitionFormat</a><br> |




UpdateDiskPartitions([devicePath](#string "string"), [spec](vim.host.DiskPartitionInfo.Specification.md "vim.host.DiskPartitionInfo.Specification"))
----------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UpdateDiskPartitions |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the device could not be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the spec is invalid. |




FormatVmfs([createSpec](vim.host.VmfsVolume.Specification.md "vim.host.VmfsVolume.Specification"))
--------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists")

---
| service name | FormatVmfs |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | if the volume name is already being used           by another volume on the host. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if VMFS version specified is not 2 or 3,           if blocksize, lock mode, or volume label are invalid,           the partition does not exist or is of an invalid type. |




MountVmfsVolume([vmfsUuid](#string "string"))
---------------------------------------------
 raises [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | MountVmfsVolume |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if VMFS Uuid is not found on the host. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if   <ul>    <li> The volume is already mounted. </li>    <li> The volume is inaccessible. </li>   </ul> |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | vim.fault.ResourceInUse |




UnmountVmfsVolume([vmfsUuid](#string "string"))
-----------------------------------------------
 raises [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UnmountVmfsVolume |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if VMFS Uuid is not found on the host. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if   <ul>    <li>The volume is already unmounted.</li>    <li>The volume is inaccessible.</li>   </ul> |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | if   <ul>    <li>There is any VM registered on this volume.</li>    <li>1 or more programs have I/O outstanding on this volume.</li>   </ul> |




DeleteVmfsVolumeState([vmfsUuid](#string "string"))
---------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | DeleteVmfsVolumeState |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for any configuration failures. |




RescanVmfs()
------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | RescanVmfs |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if configuration fails. |




AttachVmfsExtent([vmfsPath](#string "string"), [extent](vim.host.ScsiDisk.Partition.md "vim.host.ScsiDisk.Partition"))
----------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | AttachVmfsExtent |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the VMFS cannot be found or is unmounted. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the new extent is already used by another           vmfs volume, does not exist, or is of an invalid partition           type. |




ExpandVmfsExtent([vmfsPath](#string "string"), [extent](vim.host.ScsiDisk.Partition.md "vim.host.ScsiDisk.Partition"))
----------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | ExpandVmfsExtent |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the VMFS cannot be found or is unmounted. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the extent is not part of the VMFS volume. |




UpgradeVmfs([vmfsPath](#string "string"))
-----------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UpgradeVmfs |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the VMFS cannot be found or is unmounted. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if the prerequisite is not satisfied                           or for all other configuration                           failures. |




UpgradeVmLayout()
-----------------

| service name | UpgradeVmLayout |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




QueryUnresolvedVmfsVolume()
---------------------------

| service name | QueryUnresolvedVmfsVolume |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




ResolveMultipleUnresolvedVmfsVolumes([resolutionSpec](vim.host.UnresolvedVmfsResolutionSpec.md "vim.host.UnresolvedVmfsResolutionSpec"))
----------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | ResolveMultipleUnresolvedVmfsVolumes |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if batch operation fails on the host.   Because the returned array of ResolutionResult contains the new VMFS volume   or fault for each operation, as of vSphere API 5.x, we won't throw fault when   batch operation fails. |




ResolveMultipleUnresolvedVmfsVolumesEx([resolutionSpec](vim.host.UnresolvedVmfsResolutionSpec.md "vim.host.UnresolvedVmfsResolutionSpec"))
------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | ResolveMultipleUnresolvedVmfsVolumesEx |
|:--|:--|
| since version | [vSphere API 5.5](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if batch operation fails on the host.   Because the returned array of ResolutionResult contains the new VMFS volume   or fault for each operation, as of vSphere API 5.x, we won't throw fault when   batch operation fails. |




UnmountForceMountedVmfsVolume([vmfsUuid](#string "string"))
-----------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UnmountForceMountedVmfsVolume |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if VMFS Uuid is not found on the host. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |




RescanHba([hbaDevice](#string "string"))
----------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | RescanHba |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the host bus adapter cannot be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |




RescanAllHba()
--------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | RescanAllHba |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if rescan failed. |




UpdateSoftwareInternetScsiEnabled()
-----------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | UpdateSoftwareInternetScsiEnabled |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for any configuration failure. |




UpdateInternetScsiDiscoveryProperties([iScsiHbaDevice](#string "string"), [discoveryProperties](vim.host.InternetScsiHba.DiscoveryProperties.md "vim.host.InternetScsiHba.DiscoveryProperties"))
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UpdateInternetScsiDiscoveryProperties |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the host bus adapter could not be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |




UpdateInternetScsiAuthenticationProperties([iScsiHbaDevice](#string "string"), [authenticationProperties](vim.host.InternetScsiHba.AuthenticationProperties.md "vim.host.InternetScsiHba.AuthenticationProperties"), [targetSet](vim.host.InternetScsiHba.TargetSet.md "vim.host.InternetScsiHba.TargetSet"))
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UpdateInternetScsiAuthenticationProperties |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the host bus adapter could not be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |




UpdateInternetScsiDigestProperties([iScsiHbaDevice](#string "string"), [targetSet](vim.host.InternetScsiHba.TargetSet.md "vim.host.InternetScsiHba.TargetSet"), [digestProperties](vim.host.InternetScsiHba.DigestProperties.md "vim.host.InternetScsiHba.DigestProperties"))
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UpdateInternetScsiDigestProperties |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the host bus adapter could not be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |




UpdateInternetScsiAdvancedOptions([iScsiHbaDevice](#string "string"), [targetSet](vim.host.InternetScsiHba.TargetSet.md "vim.host.InternetScsiHba.TargetSet"), [options](vim.host.InternetScsiHba.ParamValue.md "vim.host.InternetScsiHba.ParamValue"))
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UpdateInternetScsiAdvancedOptions |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the host bus adapter could not be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |




UpdateInternetScsiIPProperties([iScsiHbaDevice](#string "string"), [ipProperties](vim.host.InternetScsiHba.IPProperties.md "vim.host.InternetScsiHba.IPProperties"))
--------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UpdateInternetScsiIPProperties |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the host bus adapter could not be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |




UpdateInternetScsiName([iScsiHbaDevice](#string "string"), [iScsiName](#string "string"))
-----------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UpdateInternetScsiName |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the host bus adapter could not be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |




UpdateInternetScsiAlias([iScsiHbaDevice](#string "string"), [iScsiAlias](#string "string"))
-------------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UpdateInternetScsiAlias |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the host bus adapter could not be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |




AddInternetScsiSendTargets([iScsiHbaDevice](#string "string"), [targets](vim.host.InternetScsiHba.SendTarget.md "vim.host.InternetScsiHba.SendTarget"))
-------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | AddInternetScsiSendTargets |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the discovery list could not be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |




RemoveInternetScsiSendTargets([iScsiHbaDevice](#string "string"), [targets](vim.host.InternetScsiHba.SendTarget.md "vim.host.InternetScsiHba.SendTarget"))
----------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | RemoveInternetScsiSendTargets |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if at least one target was not found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |




AddInternetScsiStaticTargets([iScsiHbaDevice](#string "string"), [targets](vim.host.InternetScsiHba.StaticTarget.md "vim.host.InternetScsiHba.StaticTarget"))
-------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | AddInternetScsiStaticTargets |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the host bus adaptor discovery list was not found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |




RemoveInternetScsiStaticTargets([iScsiHbaDevice](#string "string"), [targets](vim.host.InternetScsiHba.StaticTarget.md "vim.host.InternetScsiHba.StaticTarget"))
----------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | RemoveInternetScsiStaticTargets |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if at least one target was not found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |




EnableMultipathPath([pathName](#string "string"))
-------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | EnableMultipathPath |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the LUN could not be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |




DisableMultipathPath([pathName](#string "string"))
--------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | DisableMultipathPath |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the LUN could not be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |




SetMultipathLunPolicy([lunId](#string "string"), [policy](vim.host.MultipathInfo.LogicalUnitPolicy.md "vim.host.MultipathInfo.LogicalUnitPolicy"))
--------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | SetMultipathLunPolicy |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the LUN could not be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the policy is invalid. |




QueryPathSelectionPolicyOptions()
---------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | QueryPathSelectionPolicyOptions |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for system configuration failures. |




QueryStorageArrayTypePolicyOptions()
------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | QueryStorageArrayTypePolicyOptions |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for system configuration failures. |




UpdateScsiLunDisplayName([lunUuid](#string "string"), [displayName](#string "string"))
--------------------------------------------------------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UpdateScsiLunDisplayName |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the device could not be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the name does not meet name restrictions such           as an 80 character limit. |
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if the name does not name uniqueness restrictions.           Name uniqueness restrictions will vary based on the context in           which this method is invoked.           <p>           When this method is invoked on a host directly, no uniqueness           checks will be performed on the name.           <p>           When this method is invoked on a VC server, uniqueness checks           will be performed on the name.  The uniqueness check will           ensure that the name is unique with respect to the entire           VC instance. |




DetachScsiLun([lunUuid](#string "string"))
------------------------------------------
 raises [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | DetachScsiLun |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the device could not be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if   <ul>    <li>The device is already detached(turned 'off').        See <a href="vim.host.ScsiLun.md#operationalState">operationalState</a>.</li>   </ul> |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | if   <ul>    <li>This device is backing a Vm with a Raw Device Mapped Virtual    Disk.</li>    <li>1 or more programs have I/O outstanding on this device.</li>    <li>1 or more mounted vmfs volumes have extents residing on this    device.</li>    <li>The device is configured for use by the host e.g. diagnostic    partition is configured on this device.</li>   </ul> |




DeleteScsiLunState([lunCanonicalName](#string "string"))
--------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | DeleteScsiLunState |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for any configuration failures.<br>See <a href="vim.host.ScsiLun.md#canonicalName">canonicalName</a><br> |




AttachScsiLun([lunUuid](#string "string"))
------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | AttachScsiLun |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the device could not be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if   <ul>    <li>The device is already attached.    i.e. Device state is not 'off' in <a href="vim.host.ScsiLun.md#operationalState">operationalState</a>.</li>    <li>The device is unreachable. See <a href="vim.host.ScsiLun.md#operationalState">operationalState</a>.</li>   </ul> |




RefreshStorageSystem()
----------------------

| service name | RefreshStorageSystem |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




DiscoverFcoeHbas([fcoeSpec](vim.host.FcoeConfig.FcoeSpecification.md "vim.host.FcoeConfig.FcoeSpecification"))
--------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.FcoeFaultPnicHasNoPortSet](vim.fault.FcoeFaultPnicHasNoPortSet.md "vim.fault.FcoeFaultPnicHasNoPortSet"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | DiscoverFcoeHbas |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.FcoeFaultPnicHasNoPortSet](vim.fault.FcoeFaultPnicHasNoPortSet.md "vim.fault.FcoeFaultPnicHasNoPortSet") | vim.fault.FcoeFaultPnicHasNoPortSet |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if the host is unable to issue FCoE discovery. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the given HBA could not be found. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if any parameter in the given FcoeSpecification           is invalid. |




MarkForRemoval([hbaName](#string "string"))
-------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | MarkForRemoval |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the given HBA could not be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if the host does not support removing the given           HBA. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the given HBA is not an FCoE HBA. |




FormatVffs([createSpec](vim.host.VffsVolume.Specification.md "vim.host.VffsVolume.Specification"))
--------------------------------------------------------------------------------------------------
 raises [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists")

---
| service name | FormatVffs |
|:--|:--|
| since version | [vSphere API 5.5](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | if the volume name is already being used           by another volume on the host. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | VFFS volume is being used. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if VFFS version is invalid, the SSD disk           does not exist or is of an invalid type. |




ExtendVffs([vffsPath](#string "string"), [devicePath](#string "string"), [spec](vim.host.DiskPartitionInfo.Specification.md "vim.host.DiskPartitionInfo.Specification"))
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | ExtendVffs |
|:--|:--|
| since version | [vSphere API 5.5](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the VFFS cannot be found or is unmounted.<br>See <a href="vim.host.ScsiDisk.md#devicePath">devicePath</a><br> |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures.<br>See <a href="vim.host.ScsiDisk.md#devicePath">devicePath</a><br> |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | VFFS volume is being used.<br>See <a href="vim.host.ScsiDisk.md#devicePath">devicePath</a><br> |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the new SSD is already used by another           VFFS volume, does not exist, or is of an invalid partition           type.<br>See <a href="vim.host.ScsiDisk.md#devicePath">devicePath</a><br> |




DestroyVffs([vffsPath](#string "string"))
-----------------------------------------
 raises [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | DestroyVffs |
|:--|:--|
| since version | [vSphere API 5.5](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the VFFS cannot be found or is unmounted. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | VFFS volume is being used. |




MountVffsVolume([vffsUuid](#string "string"))
---------------------------------------------
 raises [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | MountVffsVolume |
|:--|:--|
| since version | [vSphere API 5.5](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if VFFS uuid is not found on the host. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if   <ul>    <li> The volume is already mounted. </li>    <li> The volume is inaccessible. </li>   </ul> |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | VFFS volume is being used. |




UnmountVffsVolume([vffsUuid](#string "string"))
-----------------------------------------------
 raises [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UnmountVffsVolume |
|:--|:--|
| since version | [vSphere API 5.5](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if VFFS uuid is not found on the host. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if   <ul>    <li>The volume is already unmounted.</li>    <li>The volume is inaccessible.</li>   </ul> |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | if   <ul>    <li>1 or more programs have I/O outstanding on this volume.</li>   </ul> |




DeleteVffsVolumeState([vffsUuid](#string "string"))
---------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | DeleteVffsVolumeState |
|:--|:--|
| since version | [vSphere API 5.5](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for any configuration failures. |




RescanVffs()
------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | RescanVffs |
|:--|:--|
| since version | [vSphere API 5.5](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if configuration fails. |




QueryAvailableSsds([vffsPath](#string "string"))
------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | QueryAvailableSsds |
|:--|:--|
| since version | [vSphere API 5.5](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the named VFFS volume is not found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if unable to query disk information. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if named VFFS volume is not a VFFS volume |




