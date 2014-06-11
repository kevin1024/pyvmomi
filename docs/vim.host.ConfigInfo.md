vim.host.ConfigInfo
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type encapsulates a typical set of host configuration    information that is useful for displaying and configuring a host.    <p>    VirtualCenter can retrieve this set of information    very efficiently even for a large set of hosts.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| host | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | None | None | A reference to a managed object on a host. |
| product | [vim.AboutInfo](vim.AboutInfo.md "vim.AboutInfo") | None | None | Information about a product. |
| hyperThread | [vim.host.CpuSchedulerSystem.HyperThreadScheduleInfo](vim.host.CpuSchedulerSystem.HyperThreadScheduleInfo.md "vim.host.CpuSchedulerSystem.HyperThreadScheduleInfo") | true | None | If hyperthreading is supported, this is the CPU configuration for   optimizing hyperthreading. |
| consoleReservation | [vim.host.MemoryManagerSystem.ServiceConsoleReservationInfo](vim.host.MemoryManagerSystem.ServiceConsoleReservationInfo.md "vim.host.MemoryManagerSystem.ServiceConsoleReservationInfo") | true | None | Memory configuration. |
| virtualMachineReservation | [vim.host.MemoryManagerSystem.VirtualMachineReservationInfo](vim.host.MemoryManagerSystem.VirtualMachineReservationInfo.md "vim.host.MemoryManagerSystem.VirtualMachineReservationInfo") | true | None | Virtual machine memory configuration. |
| storageDevice | [vim.host.StorageDeviceInfo](vim.host.StorageDeviceInfo.md "vim.host.StorageDeviceInfo") | true | None | Storage system information. |
| multipathState | [vim.host.MultipathStateInfo](vim.host.MultipathStateInfo.md "vim.host.MultipathStateInfo") | true | None | Storage multipath state information. |
| fileSystemVolume | [vim.host.FileSystemVolumeInfo](vim.host.FileSystemVolumeInfo.md "vim.host.FileSystemVolumeInfo") | true | None | Storage system file system volume information. |
| systemFile | string | true | None | Datastore paths of files used by the host system on   mounted volumes, for instance, the COS vmdk file of the   host. For information on datastore paths, see <a href="vim.Datastore.md">Datastore</a>. |
| network | [vim.host.NetworkInfo](vim.host.NetworkInfo.md "vim.host.NetworkInfo") | true | None | Network system information. |
| vmotion | [vim.host.VMotionInfo](vim.host.VMotionInfo.md "vim.host.VMotionInfo") | true | None | VMotion system information. |
| virtualNicManagerInfo | [vim.host.VirtualNicManagerInfo](vim.host.VirtualNicManagerInfo.md "vim.host.VirtualNicManagerInfo") | true | None | VirtualNic manager information. |
| capabilities | [vim.host.NetCapabilities](vim.host.NetCapabilities.md "vim.host.NetCapabilities") | true | None | Capability vector indicating the available network features. |
| datastoreCapabilities | [vim.host.DatastoreSystem.Capabilities](vim.host.DatastoreSystem.Capabilities.md "vim.host.DatastoreSystem.Capabilities") | true | None | Capability vector indicating available datastore features. |
| offloadCapabilities | [vim.host.NetOffloadCapabilities](vim.host.NetOffloadCapabilities.md "vim.host.NetOffloadCapabilities") | true | None | capabilities to offload operations either to the host or to physical   hardware when a virtual machine is transmitting on a network |
| service | [vim.host.ServiceInfo](vim.host.ServiceInfo.md "vim.host.ServiceInfo") | true | None | Host service configuration. |
| firewall | [vim.host.FirewallInfo](vim.host.FirewallInfo.md "vim.host.FirewallInfo") | true | None | Firewall configuration. |
| autoStart | [vim.host.AutoStartManager.Config](vim.host.AutoStartManager.Config.md "vim.host.AutoStartManager.Config") | true | None | AutoStart configuration. |
| activeDiagnosticPartition | [vim.host.DiagnosticPartition](vim.host.DiagnosticPartition.md "vim.host.DiagnosticPartition") | true | None | The diagnostic partition that will be set as the current   diagnostic partition on the host. |
| option | [vim.option.OptionValue](vim.option.OptionValue.md "vim.option.OptionValue") | true | None | Host configuration options as defined by the   <a href="vim.option.OptionValue.md">OptionValue</a> data object type. |
| optionDef | [vim.option.OptionDef](vim.option.OptionDef.md "vim.option.OptionDef") | true | None | A list of supported options. |
| datastorePrincipal | string | true | None | Datastore principal user |
| localSwapDatastore | [vim.Datastore](vim.Datastore.md "vim.Datastore") | true | None | Datastore visible to this host that may be used to store virtual   machine swapfiles, for virtual machines executing on this host. The   value of this property is set or unset by invoking   <a href="vim.host.DatastoreSystem.md#updateLocalSwapDatastore">UpdateLocalSwapDatastore</a>.   The policy for using this datastore is determined by the compute   resource configuration's   <a href="vim.ComputeResource.ConfigInfo.md#vmSwapPlacement">vmSwapPlacement</a>   property in concert with each individual virtual machine configuration's   <a href="vim.vm.ConfigInfo.md#swapPlacement">swapPlacement</a> property.   <p>   Note: Using a host-specific swap location may degrade VMotion performance. |
| systemSwapConfiguration | [vim.host.SystemSwapConfiguration](vim.host.SystemSwapConfiguration.md "vim.host.SystemSwapConfiguration") | true | None | The system swap configuration specifies which options are currently  enabled.<br/><br>See <a href="vim.host.SystemSwapConfiguration.md">HostSystemSwapConfiguration</a><br> |
| systemResources | [vim.host.SystemResourceInfo](vim.host.SystemResourceInfo.md "vim.host.SystemResourceInfo") | true | None | Reference for the system resource hierarchy, used for configuring   the set of resources reserved to the system and unavailable to   virtual machines. |
| dateTimeInfo | [vim.host.DateTimeInfo](vim.host.DateTimeInfo.md "vim.host.DateTimeInfo") | true | None | Date/Time related configuration |
| flags | [vim.host.FlagInfo](vim.host.FlagInfo.md "vim.host.FlagInfo") | true | None | Additional flags for a host. |
| adminDisabled | bool | true | None | If the flag is true, the permissions on the host have been modified such   that it is only accessible through local console or an authorized   centralized management application. This flag is affected by the   <a href="vim.HostSystem.md#enterLockdownMode">EnterLockdownMode</a> and   <a href="vim.HostSystem.md#exitLockdownMode">ExitLockdownMode</a> operations.   <p>   This flag is supported in VirtualCenter only. The value returned from host   should be ignored.<br>See <a href="vim.HostSystem.md#enterLockdownMode">EnterLockdownMode</a><br>See <a href="vim.HostSystem.md#exitLockdownMode">ExitLockdownMode</a><br> |
| ipmi | [vim.host.IpmiInfo](vim.host.IpmiInfo.md "vim.host.IpmiInfo") | true | None | IPMI (Intelligent Platform Management Interface) info for the host. |
| sslThumbprintInfo | [vim.host.SslThumbprintInfo](vim.host.SslThumbprintInfo.md "vim.host.SslThumbprintInfo") | true | None | SSL Thumbprint info for hosts registered on this host. |
| sslThumbprintData | [vim.host.SslThumbprintInfo](vim.host.SslThumbprintInfo.md "vim.host.SslThumbprintInfo") | true | None | SSL Thumbprints registered on this host. |
| certificate | int | true | None | Full Host Certificate in PEM format, if known |
| pciPassthruInfo | [vim.host.PciPassthruInfo](vim.host.PciPassthruInfo.md "vim.host.PciPassthruInfo") | true | None | PCI passthrough information. |
| authenticationManagerInfo | [vim.host.AuthenticationManagerInfo](vim.host.AuthenticationManagerInfo.md "vim.host.AuthenticationManagerInfo") | true | None | Current authentication configuration. |
| featureVersion | [vim.host.FeatureVersionInfo](vim.host.FeatureVersionInfo.md "vim.host.FeatureVersionInfo") | true | None | List of feature-specific version information. Each element refers  to the version information for a specific feature. |
| powerSystemCapability | [vim.host.PowerSystem.Capability](vim.host.PowerSystem.Capability.md "vim.host.PowerSystem.Capability") | true | None | Host power management capability. |
| powerSystemInfo | [vim.host.PowerSystem.Info](vim.host.PowerSystem.Info.md "vim.host.PowerSystem.Info") | true | None | Host power management information. |
| cacheConfigurationInfo | [vim.host.CacheConfigurationManager.CacheConfigurationInfo](vim.host.CacheConfigurationManager.CacheConfigurationInfo.md "vim.host.CacheConfigurationManager.CacheConfigurationInfo") | true | None | Host solid stats drive cache configuration information. |
| wakeOnLanCapable | bool | true | None | Indicates if a host is wake on lan capable.   A host is deemed wake on lan capable if there exists at least one   physical network card that is both backing the vmotion interface and   is itself wake on lan capable. |
| featureCapability | [vim.host.FeatureCapability](vim.host.FeatureCapability.md "vim.host.FeatureCapability") | true | None | Array of the feature capabilities that the host has. This is not   expected to change after the host boots. It may change between reboots   in the case BIOS options are changed, or hardware, or firmware is   changed or upgraded. |
| maskedFeatureCapability | [vim.host.FeatureCapability](vim.host.FeatureCapability.md "vim.host.FeatureCapability") | true | None | Array of the feature capabilities that the host has after the   mask has been applied. |
| vFlashConfigInfo | [vim.host.VFlashManager.VFlashConfigInfo](vim.host.VFlashManager.VFlashConfigInfo.md "vim.host.VFlashManager.VFlashConfigInfo") | true | None | Host vFlash configuration information |
| vsanHostConfig | [vim.vsan.host.ConfigInfo](vim.vsan.host.ConfigInfo.md "vim.vsan.host.ConfigInfo") | true | None | VSAN configuration for a host. |
| graphicsInfo | [vim.host.GraphicsInfo](vim.host.GraphicsInfo.md "vim.host.GraphicsInfo") | true | None | The list of graphics devices available on this host. |


