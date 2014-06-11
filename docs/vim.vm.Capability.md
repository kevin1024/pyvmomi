vim.vm.Capability
=================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type contains information about the  operation/capabilities of a virtual machine

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| snapshotOperationsSupported | bool | None | None | Indicates whether or not a virtual machine supports snapshot operations. |
| multipleSnapshotsSupported | bool | None | None | Indicates whether or not a virtual machine supports multiple snapshots.  This value is not set when the virtual machine is unavailable, for instance,  when it is being created or deleted. |
| snapshotConfigSupported | bool | None | None | Indicates whether or not a virtual machine supports snapshot config. |
| poweredOffSnapshotsSupported | bool | None | None | Indicates whether or not a virtual machine supports snapshot operations in  poweredOff state. This flag doesn't affect vim.VirtualMachine.GetSnapshot,  which is always supported. |
| memorySnapshotsSupported | bool | None | None | Indicates whether or not a virtual machine supports memory snapshots. |
| revertToSnapshotSupported | bool | None | None | Indicates whether or not a virtual machine supports reverting to a snapshot. |
| quiescedSnapshotsSupported | bool | None | None | Indicates whether or not a virtual machine supports quiesced snapshots. |
| disableSnapshotsSupported | bool | None | None | Indicates whether or not snapshots can be disabled. |
| lockSnapshotsSupported | bool | None | None | Indicates whether or not the snapshot tree can be locked. |
| consolePreferencesSupported | bool | None | None | Indicates whether console preferences can be set for this virtual machine. |
| cpuFeatureMaskSupported | bool | None | None | Indicates whether CPU feature requirements masks can be set for this  virtual machine. |
| s1AcpiManagementSupported | bool | None | None | Indicates whether or not a virtual machine supports ACPI S1 settings management. |
| settingScreenResolutionSupported | bool | None | None | Indicates whether of not this virtual machine supports  setting the screen resolution of the console window.  This capability depends on the guest operating system  configured for this virtual machine. |
| toolsAutoUpdateSupported | bool | None | None | Supports tools auto-update. |
| vmNpivWwnSupported | bool | None | None | Supports virtual machine NPIV WWN. |
| npivWwnOnNonRdmVmSupported | bool | None | None | Supports assigning NPIV WWN to virtual machines that don't have RDM disks. |
| vmNpivWwnDisableSupported | bool | None | None | Indicates whether the NPIV disabling operation is supported the virtual machine. |
| vmNpivWwnUpdateSupported | bool | None | None | Indicates whether the update of NPIV WWNs are supported on the virtual machine. |
| swapPlacementSupported | bool | None | None | Flag indicating whether the virtual machine has a configurable   <a href="vim.vm.ConfigInfo.md#swapPlacement">swapfile placement policy</a>. |
| toolsSyncTimeSupported | bool | None | None | Indicates whether asking tools to sync time with the host is supported. |
| virtualMmuUsageSupported | bool | None | None | Indicates whether or not the use of nested page table hardware support   can be explicitly set. |
| diskSharesSupported | bool | None | None | Indicates whether resource settings for disks can be   applied to this virtual machine. |
| bootOptionsSupported | bool | None | None | Indicates whether boot options can be configured   for this virtual machine. |
| bootRetryOptionsSupported | bool | None | None | Indicates whether automatic boot retry can be   configured for this virtual machine. |
| settingVideoRamSizeSupported | bool | None | None | Flag indicating whether the video ram size of this virtual machine   can be configured. |
| settingDisplayTopologySupported | bool | None | None | Indicates whether of not this virtual machine supports  setting the display topology of the console window.  This capability depends on the guest operating system  configured for this virtual machine. |
| recordReplaySupported | bool | None | None | Indicates whether record and replay functionality is supported on this  virtual machine. |
| changeTrackingSupported | bool | None | None | Indicates that change tracking is supported for virtual disks of this  virtual machine. However, even if change tracking is supported, it might  not be available for all disks of the virtual machine. For example,  passthru raw disk mappings or disks backed by any Ver1BackingInfo cannot  be tracked. |
| multipleCoresPerSocketSupported | bool | None | None | Indicates whether multiple virtual cores per socket is supported on this VM. |
| hostBasedReplicationSupported | bool | None | None | Indicates that host based replication is supported on this virtual  machine. However, even if host based replication is supported,  it might not be available for all disk types. For example, passthru  raw disk mappings can not be replicated. |
| guestAutoLockSupported | bool | None | None |  |
| memoryReservationLockSupported | bool | None | None | Indicates whether  <a href="vim.vm.ConfigInfo.md#memoryReservationLockedToMax">memoryReservationLockedToMax</a>  may be set to true for this virtual machine. |
| featureRequirementSupported | bool | None | None | Indicates whether featureRequirement feature is supported. |
| poweredOnMonitorTypeChangeSupported | bool | None | None | Indicates whether a monitor type change is supported while this virtual  machine is in the poweredOn state. |
| seSparseDiskSupported | bool | None | None | Indicates whether this virtual machine supports the Flex-SE  (space-efficent, sparse) format for virtual disks. |
| nestedHVSupported | bool | None | None | Indicates whether this virtual machine supports nested hardware-assisted   virtualization. |
| vPMCSupported | bool | None | None | Indicates whether this virtual machine supports virtualized CPU performance  counters. |


