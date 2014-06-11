vim.host.ConfigManager
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes the configuration of a host   across products and versions.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| cpuScheduler | [vim.host.CpuSchedulerSystem](vim.host.CpuSchedulerSystem.md "vim.host.CpuSchedulerSystem") | true | None | The CPU scheduler that determines which threads execute on a CPU   at any given time. |
| datastoreSystem | [vim.host.DatastoreSystem](vim.host.DatastoreSystem.md "vim.host.DatastoreSystem") | true | None | The datastore manager. |
| memoryManager | [vim.host.MemoryManagerSystem](vim.host.MemoryManagerSystem.md "vim.host.MemoryManagerSystem") | true | None | The memory manager on the host. |
| storageSystem | [vim.host.StorageSystem](vim.host.StorageSystem.md "vim.host.StorageSystem") | true | None | The storage configuration. |
| networkSystem | [vim.host.NetworkSystem](vim.host.NetworkSystem.md "vim.host.NetworkSystem") | true | None | The network system configuration. |
| vmotionSystem | [vim.host.VMotionSystem](vim.host.VMotionSystem.md "vim.host.VMotionSystem") | true | None | The VMotion configuration. |
| virtualNicManager | [vim.host.VirtualNicManager](vim.host.VirtualNicManager.md "vim.host.VirtualNicManager") | true | None | The VirtualNic configuration. |
| serviceSystem | [vim.host.ServiceSystem](vim.host.ServiceSystem.md "vim.host.ServiceSystem") | true | None | The configuration of the host services (for example,   SSH, FTP, and Telnet). |
| firewallSystem | [vim.host.FirewallSystem](vim.host.FirewallSystem.md "vim.host.FirewallSystem") | true | None | The firewall configuration. |
| advancedOption | [vim.option.OptionManager](vim.option.OptionManager.md "vim.option.OptionManager") | true | None | Advanced options. |
| diagnosticSystem | [vim.host.DiagnosticSystem](vim.host.DiagnosticSystem.md "vim.host.DiagnosticSystem") | true | None | The diagnostic for the ESX Server system. |
| autoStartManager | [vim.host.AutoStartManager](vim.host.AutoStartManager.md "vim.host.AutoStartManager") | true | None | Auto-start and auto-stop configuration. |
| snmpSystem | [vim.host.SnmpSystem](vim.host.SnmpSystem.md "vim.host.SnmpSystem") | true | None | Snmp configuration |
| dateTimeSystem | [vim.host.DateTimeSystem](vim.host.DateTimeSystem.md "vim.host.DateTimeSystem") | true | None | DateTime configuration |
| patchManager | [vim.host.PatchManager](vim.host.PatchManager.md "vim.host.PatchManager") | true | None | Host patch management. |
| imageConfigManager | [vim.host.ImageConfigManager](vim.host.ImageConfigManager.md "vim.host.ImageConfigManager") | true | None | Host image configuration management. |
| bootDeviceSystem | [vim.host.BootDeviceSystem](vim.host.BootDeviceSystem.md "vim.host.BootDeviceSystem") | true | None | Boot device order management. |
| firmwareSystem | [vim.host.FirmwareSystem](vim.host.FirmwareSystem.md "vim.host.FirmwareSystem") | true | None | Firmware management. |
| healthStatusSystem | [vim.host.HealthStatusSystem](vim.host.HealthStatusSystem.md "vim.host.HealthStatusSystem") | true | None | System health status manager. |
| pciPassthruSystem | [vim.host.PciPassthruSystem](vim.host.PciPassthruSystem.md "vim.host.PciPassthruSystem") | true | None | PciDeviceSystem for passthru. |
| licenseManager | [vim.LicenseManager](vim.LicenseManager.md "vim.LicenseManager") | true | None | License manager |
| kernelModuleSystem | [vim.host.KernelModuleSystem](vim.host.KernelModuleSystem.md "vim.host.KernelModuleSystem") | true | None | Kernel module configuration management. |
| authenticationManager | [vim.host.AuthenticationManager](vim.host.AuthenticationManager.md "vim.host.AuthenticationManager") | true | None | Authentication method configuration - for example, for Active Directory membership. |
| powerSystem | [vim.host.PowerSystem](vim.host.PowerSystem.md "vim.host.PowerSystem") | true | None | Power System manager. |
| cacheConfigurationManager | [vim.host.CacheConfigurationManager](vim.host.CacheConfigurationManager.md "vim.host.CacheConfigurationManager") | true | None | Host solid state drive cache configuration manager. |
| esxAgentHostManager | [vim.host.EsxAgentHostManager](vim.host.EsxAgentHostManager.md "vim.host.EsxAgentHostManager") | true | None | Esx Agent resource configuration manager |
| iscsiManager | [vim.host.IscsiManager](vim.host.IscsiManager.md "vim.host.IscsiManager") | true | None | Iscsi Management Operations managed entity |
| vFlashManager | [vim.host.VFlashManager](vim.host.VFlashManager.md "vim.host.VFlashManager") | true | None | vFlash Manager |
| vsanSystem | [vim.host.VsanSystem](vim.host.VsanSystem.md "vim.host.VsanSystem") | true | None | VsanSystem managed entity. |
| graphicsManager | [vim.host.GraphicsManager](vim.host.GraphicsManager.md "vim.host.GraphicsManager") | true | None | Host graphics manager. |
| vsanInternalSystem | [vim.host.VsanInternalSystem](vim.host.VsanInternalSystem.md "vim.host.VsanInternalSystem") | true | None | VsanInternalSystem managed entity. |


