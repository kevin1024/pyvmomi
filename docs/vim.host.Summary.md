vim.host.Summary
================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type encapsulates a typical set of host information that is useful   for list views and summary pages.   <p>   VirtualCenter can retrieve this information very efficiently, even for a large set   of hosts.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| host | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | true | None | The reference to the host-managed object. |
| hardware | [vim.host.Summary.HardwareSummary](vim.host.Summary.HardwareSummary.md "vim.host.Summary.HardwareSummary") | true | None | Basic hardware information, if known. |
| runtime | [vim.host.RuntimeInfo](vim.host.RuntimeInfo.md "vim.host.RuntimeInfo") | true | None | Basic runtime information, if known. |
| config | [vim.host.Summary.ConfigSummary](vim.host.Summary.ConfigSummary.md "vim.host.Summary.ConfigSummary") | None | None | Basic configuration information, if known. |
| quickStats | [vim.host.Summary.QuickStats](vim.host.Summary.QuickStats.md "vim.host.Summary.QuickStats") | None | None | Basic host statistics. |
| overallStatus | [vim.ManagedEntity.Status](vim.ManagedEntity.Status.md "vim.ManagedEntity.Status") | None | None | The overall alarm status of the host.    In releases after vSphere API 5.0, vSphere Servers might not   generate property collector update notifications for this property.   To obtain the latest value of the property, you can use   PropertyCollector methods RetrievePropertiesEx or WaitForUpdatesEx.   If you use the PropertyCollector.WaitForUpdatesEx method, specify   an empty string for the version parameter.    Since this property is on a DataObject, an update returned by WaitForUpdatesEx may   contain values for this property when some other property on the DataObject changes.   If this update is a result of a call to WaitForUpdatesEx with a non-empty   version parameter, the value for this property may not be current. |
| rebootRequired | bool | None | None | Indicates whether or not the host requires a reboot due to a configuration   change. |
| customValue | [vim.CustomFieldsManager.Value](vim.CustomFieldsManager.Value.md "vim.CustomFieldsManager.Value") | true | None | The customized field values. |
| managementServerIp | string | true | None | IP address of the VirtualCenter server managing this host, if any. |
| maxEVCModeKey | string | true | None | The most capable Enhanced VMotion Compatibility mode supported by the   host hardware and software; unset if this host cannot participate in   any EVC mode.<br>See <a href="vim.Capability.md#supportedEVCMode">supportedEVCMode</a><br> |
| currentEVCModeKey | string | true | None | The Enhanced VMotion Compatibility mode that is currently in effect   for this host. If the host is in a cluster where EVC is active, this   will match the cluster's EVC mode; otherwise this will be unset.<br>See <a href="vim.Capability.md#supportedEVCMode">supportedEVCMode</a><br> |


