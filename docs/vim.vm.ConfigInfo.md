vim.vm.ConfigInfo
=================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The ConfigInfo data object type encapsulates the configuration settings and   virtual hardware for a virtual machine. This type holds all the information   that is present in the .vmx configuration file for the virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| changeVersion | string | None | None | The changeVersion is a unique identifier for a given version    of the configuration. Each change to the configuration    updates this value. This is typically implemented as an ever    increasing count or a time-stamp. However, a client should    always treat this as an opaque string. |
| modified | datetime | None | None | Last time a virtual machine's configuration was modified. |
| name | string | None | None | Display name of the virtual machine.   <p>   Any / (slash), \ (backslash), character used in this   name element is escaped. Similarly, any % (percent) character used in  this name element is escaped, unless it is used to start an escape   sequence. A slash is escaped as %2F or %2f. A backslash is escaped as %5C or   %5c, and a percent is escaped as %25. |
| guestFullName | string | None | None | This is the full name of the guest operating system for the virtual machine.   For example: Windows 2000 Professional.  <p><br>See <a href="vim.vm.ConfigInfo.md#alternateGuestName">alternateGuestName</a><br> |
| version | string | None | None | The version string for this virtual machine. |
| uuid | string | None | None | 128-bit SMBIOS UUID of a virtual machine represented as a hexadecimal string   in "12345678-abcd-1234-cdef-123456789abc" format. |
| instanceUuid | string | true | None | VirtualCenter-specific 128-bit UUID of a virtual machine, represented   as a hexademical string. This identifier is used by VirtualCenter to   uniquely identify all virtual machine instances, including those that   may share the same SMBIOS UUID. |
| npivNodeWorldWideName | long | true | None | A 64-bit node WWN (World Wide Name). These WWNs are paired with the   <a href="vim.vm.ConfigInfo.md#npivPortWorldWideName">npivPortWorldWideName</a> to be used by the NPIV VPORTs instantiated for the   virtual machine on the physical HBAs of the host. A pair of node and port WWNs   serves as a unique identifier in accessing a LUN, so that it can be monitored or   controlled by the storage administrator.   <p>   If this property contains a single node WWN, the same node WWN is used to pair   with all port WWNs listed in <a href="vim.vm.ConfigInfo.md#npivPortWorldWideName">npivPortWorldWideName</a>. If this property or   <a href="vim.vm.ConfigInfo.md#npivPortWorldWideName">npivPortWorldWideName</a> is empty or unset, NPIV WWN is disabled for the   virtual machine. |
| npivPortWorldWideName | long | true | None | A 64-bit port WWN (World Wide Name). For detail description on WWN, see  <a href="vim.vm.ConfigInfo.md#npivNodeWorldWideName">npivNodeWorldWideName</a>. |
| npivWorldWideNameType | string | true | None | The source that provides/generates the assigned WWNs.   <p><br>See <a href="vim.vm.ConfigInfo.NpivWwnType.md">VirtualMachineConfigInfoNpivWwnType</a><br> |
| npivDesiredNodeWwns | short | true | None | The NPIV node WWNs to be extended from the original list of WWN nummbers. This   property should be set to desired number which is an aggregate of existing   plus new numbers. Desired Node WWNs should always be greater than the existing   number of node WWNs |
| npivDesiredPortWwns | short | true | None | The NPIV port WWNs to be extended from the original list of WWN nummbers. This   property should be set to desired number which is an aggregate of existing   plus new numbers. Desired Node WWNs should always be greater than the existing   number of port WWNs |
| npivTemporaryDisabled | bool | true | None | This property is used to enable or disable the NPIV capability on a desired   virtual machine on a temporary basis. When this property is set NPIV Vport   will not be instantiated by the VMX process of the Virtual Machine. When this   property is set port WWNs and node WWNs in the VM configuration are preserved. |
| npivOnNonRdmDisks | bool | true | None | This property is used to check whether the NPIV can be enabled on the Virtual   machine with non-rdm disks in the configuration, so this is potentially not   enabling npiv on vmfs disks. Also this property is used to check whether RDM   is required to generate WWNs for a virtual machine. |
| locationId | string | true | None | Hash incorporating the virtual machine's config file location   and the UUID of the host assigned to run the virtual machine. |
| template | bool | None | None | Flag indicating whether or not a virtual machine is a template. |
| guestId | string | None | None | Guest operating system configured on a virtual machine.   This is a guest identifier that can be used to access the   <a href="vim.vm.GuestOsDescriptor.md">GuestOsDescriptor</a>   list for information about default configuration.   For more information on possible values, see   <a href="vim.vm.GuestOsDescriptor.GuestOsIdentifier.md">VirtualMachineGuestOsIdentifier</a>. |
| alternateGuestName | string | None | None | Used as display name for the operating system if guestId is <tt>other</tt>   or <tt>other-64</tt>.   <p><br>See <a href="vim.vm.ConfigInfo.md#guestFullName">guestFullName</a><br> |
| annotation | string | true | None | Description for the virtual machine. |
| files | [vim.vm.FileInfo](vim.vm.FileInfo.md "vim.vm.FileInfo") | None | None | Information about the files associated with a virtual machine.   This information does not include files for specific virtual disks or   snapshots. |
| tools | [vim.vm.ToolsConfigInfo](vim.vm.ToolsConfigInfo.md "vim.vm.ToolsConfigInfo") | true | None | Configuration of VMware Tools running in the guest operating system. |
| flags | [vim.vm.FlagInfo](vim.vm.FlagInfo.md "vim.vm.FlagInfo") | None | None | Additional flags for a virtual machine. |
| consolePreferences | [vim.vm.ConsolePreferences](vim.vm.ConsolePreferences.md "vim.vm.ConsolePreferences") | true | None | Legacy console viewer preferences when doing power operations. |
| defaultPowerOps | [vim.vm.DefaultPowerOpInfo](vim.vm.DefaultPowerOpInfo.md "vim.vm.DefaultPowerOpInfo") | None | None | Configuration of default power operations. |
| hardware | [vim.vm.VirtualHardware](vim.vm.VirtualHardware.md "vim.vm.VirtualHardware") | None | None | Processor, memory, and virtual devices for a virtual machine. |
| cpuAllocation | [vim.ResourceAllocationInfo](vim.ResourceAllocationInfo.md "vim.ResourceAllocationInfo") | true | None | Resource limits for CPU. |
| memoryAllocation | [vim.ResourceAllocationInfo](vim.ResourceAllocationInfo.md "vim.ResourceAllocationInfo") | true | None | Resource limits for memory. |
| latencySensitivity | [vim.LatencySensitivity](vim.LatencySensitivity.md "vim.LatencySensitivity") | true | None | The latency-sensitivity of the virtual machine. |
| memoryHotAddEnabled | bool | true | None | Whether memory can be added while this virtual machine is running. |
| cpuHotAddEnabled | bool | true | None | Whether virtual processors can be added while this   virtual machine is running. |
| cpuHotRemoveEnabled | bool | true | None | Whether virtual processors can be removed while this   virtual machine is running. |
| hotPlugMemoryLimit | long | true | None | The maximum amount of memory, in MB, than can be added to a   running virtual machine. This value is determined by the   virtual machine and is specified only if   <a href="vim.vm.ConfigInfo.md#memoryHotAddEnabled">memoryHotAddEnabled</a>   is set to true. |
| hotPlugMemoryIncrementSize | long | true | None | Memory, in MB that can be added to a running virtual machine   must be in increments of this value and needs be a   multiple of this value.    This value is determined by the virtual machine and is specified   only if <a href="vim.vm.ConfigSpec.md#memoryHotAddEnabled">memoryHotAddEnabled</a>   has been set to true. |
| cpuAffinity | [vim.vm.AffinityInfo](vim.vm.AffinityInfo.md "vim.vm.AffinityInfo") | true | None | Affinity settings for CPU. |
| memoryAffinity | [vim.vm.AffinityInfo](vim.vm.AffinityInfo.md "vim.vm.AffinityInfo") | true | None | Affinity settings for memory. |
| networkShaper | [vim.vm.NetworkShaperInfo](vim.vm.NetworkShaperInfo.md "vim.vm.NetworkShaperInfo") | true | None | Resource limits for network. |
| extraConfig | [vim.option.OptionValue](vim.option.OptionValue.md "vim.option.OptionValue") | true | None | Additional configuration information for the virtual machine. |
| cpuFeatureMask | [vim.host.CpuIdInfo](vim.host.CpuIdInfo.md "vim.host.CpuIdInfo") | true | None | Specifies CPU feature compatibility masks that override the   defaults from the <a href="vim.vm.GuestOsDescriptor.md">GuestOsDescriptor</a>   of the virtual machine's guest OS. |
| datastoreUrl | [vim.vm.ConfigInfo.DatastoreUrlPair](vim.vm.ConfigInfo.DatastoreUrlPair.md "vim.vm.ConfigInfo.DatastoreUrlPair") | true | None | Enumerates the set of datastores that this virtual machine is   stored on, as well as the URL identification for each of these.   <p>   Changes to datastores do not generate property updates on this   property. However, when this property is retrieved it returns the   current datastore information. |
| swapPlacement | string | true | None | Virtual machine swapfile placement policy. This will be unset if the   virtual machine's   <a href="vim.vm.Capability.md#swapPlacementSupported">swapPlacementSupported</a>   capability is false. If swapPlacementSupported is true, the default   policy is "inherit".   <p><br>See <a href="vim.vm.ConfigInfo.SwapPlacementType.md">VirtualMachineConfigInfoSwapPlacementType</a><br> |
| bootOptions | [vim.vm.BootOptions](vim.vm.BootOptions.md "vim.vm.BootOptions") | true | None | Configuration options for the boot behavior of the virtual machine. |
| ftInfo | [vim.vm.FaultToleranceConfigInfo](vim.vm.FaultToleranceConfigInfo.md "vim.vm.FaultToleranceConfigInfo") | true | None | Fault Tolerance settings for this virtual machine. |
| vAppConfig | [vim.vApp.VmConfigInfo](vim.vApp.VmConfigInfo.md "vim.vApp.VmConfigInfo") | true | None | vApp meta-data for the virtual machine |
| vAssertsEnabled | bool | true | None | Indicates whether user-configured virtual asserts will be   triggered during virtual machine replay. |
| changeTrackingEnabled | bool | true | None | Indicates whether changed block tracking for this VM's disks  is active. |
| firmware | string | true | None | Information about firmware type for this Virtual Machine.    Possible values are described in   <a href="vim.vm.GuestOsDescriptor.FirmwareType.md">GuestOsDescriptorFirmwareType</a> |
| maxMksConnections | int | true | None | Indicates the maximum number of active remote display connections  that the virtual machine will support. |
| guestAutoLockEnabled | bool | true | None | Indicates whether the guest operating system will logout any active  sessions whenever there are no remote display connections open to  the virtual machine. |
| managedBy | [vim.ext.ManagedByInfo](vim.ext.ManagedByInfo.md "vim.ext.ManagedByInfo") | true | None | Specifies that this VM is managed by a VC Extension. See the  <a href="vim.vm.ConfigSpec.md#managedBy">managedBy</a> property in the ConfigSpec  for more details. |
| memoryReservationLockedToMax | bool | true | None | If set true, memory resource reservation for this virtual machine will always be  equal to the virtual machine's memory size; increases in memory size will be  rejected when a corresponding reservation increase is not possible. |
| initialOverhead | [vim.vm.ConfigInfo.OverheadInfo](vim.vm.ConfigInfo.OverheadInfo.md "vim.vm.ConfigInfo.OverheadInfo") | true | None | Set of values to be used only to perform admission control when  determining if a host has sufficient resources for the virtual  machine to power on. |
| nestedHVEnabled | bool | true | None | Indicates whether this VM is configured to use nested  hardware-assisted virtualization. |
| vPMCEnabled | bool | true | None | Indicates whether this VM have vurtual CPU performance counters   enabled. |
| scheduledHardwareUpgradeInfo | [vim.vm.ScheduledHardwareUpgradeInfo](vim.vm.ScheduledHardwareUpgradeInfo.md "vim.vm.ScheduledHardwareUpgradeInfo") | true | None | Configuration of scheduled hardware upgrades and result from last   attempt to run scheduled hardware upgrade.<br>See <a href="vim.vm.ScheduledHardwareUpgradeInfo.md">ScheduledHardwareUpgradeInfo</a><br> |
| vFlashCacheReservation | long | true | None | Specifies the total vFlash resource reservation for the vFlash caches associated  with this VM's virtual disks, in bytes. This reservation must be allocated to power on the VM.  See <a href="vim.vm.RuntimeInfo.md#vFlashCacheAllocation">vFlashCacheAllocation</a> for allocated  reservation when VM is powered on. |


