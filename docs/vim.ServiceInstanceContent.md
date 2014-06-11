vim.ServiceInstanceContent
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The <a href="vim.ServiceInstanceContent.md">ServiceContent</a> data object defines properties for the ServiceInstance   managed object. The ServiceInstance itself does not have directly-accessible   properties because reading the properties of a managed object requires   the use of a property collector, and the property collector itself   is a property of the <a href="vim.ServiceInstance.md">ServiceInstance</a>.    For this reason, use the method <a href="vim.ServiceInstance.md#retrieveContent">RetrieveServiceContent</a>   to retrieve the <a href="vim.ServiceInstanceContent.md">ServiceContent</a> object.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| rootFolder | [vim.Folder](vim.Folder.md "vim.Folder") | None | None | Reference to the top of the inventory managed by this service. |
| propertyCollector | [vmodl.query.PropertyCollector](vmodl.query.PropertyCollector.md "vmodl.query.PropertyCollector") | None | None | Reference to a per-session object for retrieving properties and updates. |
| viewManager | [vim.view.ViewManager](vim.view.ViewManager.md "vim.view.ViewManager") | true | None | A singleton managed object for tracking custom sets of objects. |
| about | [vim.AboutInfo](vim.AboutInfo.md "vim.AboutInfo") | None | None | Information about the service, such as the software version. |
| setting | [vim.option.OptionManager](vim.option.OptionManager.md "vim.option.OptionManager") | true | None | Generic configuration for a management server. This is for example by   vCenter to store the vCenter Settings. This is not used for a   stand-alone host, instead the vim.host.ConfigManager.advancedOption is used.<br>See <a href="vim.host.ConfigManager.md">HostConfigManager</a><br> |
| userDirectory | [vim.UserDirectory](vim.UserDirectory.md "vim.UserDirectory") | true | None | A user directory managed object. |
| sessionManager | [vim.SessionManager](vim.SessionManager.md "vim.SessionManager") | true | None | Managed object for logging in and managing sessions. |
| authorizationManager | [vim.AuthorizationManager](vim.AuthorizationManager.md "vim.AuthorizationManager") | true | None | Manages permissions for managed entities in the service. |
| serviceManager | [vim.ServiceManager](vim.ServiceManager.md "vim.ServiceManager") | true | None | A singleton managed object that manages local services. |
| perfManager | [vim.PerformanceManager](vim.PerformanceManager.md "vim.PerformanceManager") | true | None | A singleton managed object that manages the collection and reporting   of performance statistics. |
| scheduledTaskManager | [vim.scheduler.ScheduledTaskManager](vim.scheduler.ScheduledTaskManager.md "vim.scheduler.ScheduledTaskManager") | true | None | A singleton managed object that manages scheduled tasks. |
| alarmManager | [vim.alarm.AlarmManager](vim.alarm.AlarmManager.md "vim.alarm.AlarmManager") | true | None | A singleton managed object that manages alarms. |
| eventManager | [vim.event.EventManager](vim.event.EventManager.md "vim.event.EventManager") | true | None | A singleton managed object that manages events. |
| taskManager | [vim.TaskManager](vim.TaskManager.md "vim.TaskManager") | true | None | A singleton managed object that manages tasks. |
| extensionManager | [vim.ExtensionManager](vim.ExtensionManager.md "vim.ExtensionManager") | true | None | A singleton managed object that manages extensions. |
| customizationSpecManager | [vim.CustomizationSpecManager](vim.CustomizationSpecManager.md "vim.CustomizationSpecManager") | true | None | A singleton managed object that manages saved guest customization   specifications. |
| customFieldsManager | [vim.CustomFieldsManager](vim.CustomFieldsManager.md "vim.CustomFieldsManager") | true | None | A singleton managed object that managed custom fields. |
| accountManager | [vim.host.LocalAccountManager](vim.host.LocalAccountManager.md "vim.host.LocalAccountManager") | true | None | A singleton managed object that manages host local user and group accounts. |
| diagnosticManager | [vim.DiagnosticManager](vim.DiagnosticManager.md "vim.DiagnosticManager") | true | None | A singleton managed object that provides access to low-level log files. |
| licenseManager | [vim.LicenseManager](vim.LicenseManager.md "vim.LicenseManager") | true | None | A singleton managed object that manages licensing |
| searchIndex | [vim.SearchIndex](vim.SearchIndex.md "vim.SearchIndex") | true | None | A singleton managed object that allows search of the inventory |
| fileManager | [vim.FileManager](vim.FileManager.md "vim.FileManager") | true | None | A singleton managed object that allows management of files present   on datastores. |
| datastoreNamespaceManager | [vim.DatastoreNamespaceManager](vim.DatastoreNamespaceManager.md "vim.DatastoreNamespaceManager") | true | None | Datastore Namespace manager.   A singleton managed object that is used to manage manipulations  related to datastores' namespaces. |
| virtualDiskManager | [vim.VirtualDiskManager](vim.VirtualDiskManager.md "vim.VirtualDiskManager") | true | None | A singleton managed object that allows management of virtual disks   on datastores. |
| virtualizationManager | [vim.VirtualizationManager](vim.VirtualizationManager.md "vim.VirtualizationManager") | true | None | A singleton managed object that manages the discovery, analysis,   recommendation and virtualization of physical machines |
| snmpSystem | [vim.host.SnmpSystem](vim.host.SnmpSystem.md "vim.host.SnmpSystem") | true | None | A singleton managed object that allows SNMP configuration.   Not set if not supported on a particular platform. |
| vmProvisioningChecker | [vim.vm.check.ProvisioningChecker](vim.vm.check.ProvisioningChecker.md "vim.vm.check.ProvisioningChecker") | true | None | A singleton managed object that can answer questions about the   feasibility of certain provisioning operations. |
| vmCompatibilityChecker | [vim.vm.check.CompatibilityChecker](vim.vm.check.CompatibilityChecker.md "vim.vm.check.CompatibilityChecker") | true | None | A singleton managed object that can answer questions about compatibility   of a virtual machine with a host. |
| ovfManager | [vim.OvfManager](vim.OvfManager.md "vim.OvfManager") | true | None | A singleton managed object that can generate OVF descriptors (export) and create  vApps (single-VM or vApp container-based) from OVF descriptors (import). |
| ipPoolManager | [vim.IpPoolManager](vim.IpPoolManager.md "vim.IpPoolManager") | true | None | A singleton managed object that supports management of IpPool objects. IP pools are  used when allocating IPv4 and IPv6 addresses to vApps. |
| dvSwitchManager | [vim.dvs.DistributedVirtualSwitchManager](vim.dvs.DistributedVirtualSwitchManager.md "vim.dvs.DistributedVirtualSwitchManager") | true | None | A singleton managed object that provides relevant information of   DistributedVirtualSwitch. |
| hostProfileManager | [vim.profile.host.ProfileManager](vim.profile.host.ProfileManager.md "vim.profile.host.ProfileManager") | true | None | A singleton managed object that manages the host profiles. |
| clusterProfileManager | [vim.profile.cluster.ProfileManager](vim.profile.cluster.ProfileManager.md "vim.profile.cluster.ProfileManager") | true | None | A singleton managed object that manages the cluster profiles. |
| complianceManager | [vim.profile.ComplianceManager](vim.profile.ComplianceManager.md "vim.profile.ComplianceManager") | true | None | A singleton managed object that manages compliance aspects of entities. |
| localizationManager | [vim.LocalizationManager](vim.LocalizationManager.md "vim.LocalizationManager") | true | None | A singleton managed object that provides methods for retrieving message  catalogs for client-side localization support. |
| storageResourceManager | [vim.StorageResourceManager](vim.StorageResourceManager.md "vim.StorageResourceManager") | true | None | A singleton managed object that provides methods for storage resource  management. |
| guestOperationsManager | [vim.vm.guest.GuestOperationsManager](vim.vm.guest.GuestOperationsManager.md "vim.vm.guest.GuestOperationsManager") | true | None | A singleton managed object that provides methods for guest operations. |


