vim.HostSystem
==============
inherits from [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity")


The HostSystem managed object type provides access to a virtualization   host platform.   <p>   Invoking destroy on a HostSystem of standalone type throws a NotSupported fault.   A standalone HostSystem can be destroyed only by invoking destroy on its parent   ComputeResource.   Invoking destroy on a failover host throws a   <a href="vim.fault.DisallowedOperationOnFailoverHost.md">DisallowedOperationOnFailoverHost</a> fault. See   <a href="vim.cluster.FailoverHostAdmissionControlPolicy.md">ClusterFailoverHostAdmissionControlPolicy</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='runtime'>runtime</a> | [vim.host.RuntimeInfo](vim.host.RuntimeInfo.md "vim.host.RuntimeInfo") | None | None | Runtime state information about the host such as connection state. |
| <a href='summary'>summary</a> | [vim.host.Summary](vim.host.Summary.md "vim.host.Summary") | None | None | Basic information about the host, including connection state. |
| <a href='hardware'>hardware</a> | [vim.host.HardwareInfo](vim.host.HardwareInfo.md "vim.host.HardwareInfo") | true | None | Hardware configuration of the host. This might not be available for a   disconnected host. |
| <a href='capability'>capability</a> | [vim.host.Capability](vim.host.Capability.md "vim.host.Capability") | true | None | Host capabilities. This might not be available for a   disconnected host. |
| <a href='licensableResource'>licensableResource</a> | [vim.LicenseManager.LicensableResourceInfo](vim.LicenseManager.LicensableResourceInfo.md "vim.LicenseManager.LicensableResourceInfo") | None | None | Information about all licensable resources, currently present on this host.  <p>This information is used mostly by the modules, manipulating information  in the <a href="vim.LicenseManager.md">LicenseManager</a>. Developers of such modules  should use this property instead of <a href="vim.HostSystem.md#hardware">hardware</a>.  <p>NOTE:    The values in this property may not be accurate for pre-5.0 hosts when returned by vCenter 5.0 |
| <a href='configManager'>configManager</a> | [vim.host.ConfigManager](vim.host.ConfigManager.md "vim.host.ConfigManager") | None | None | Host configuration systems.    In releases after vSphere API 5.0, vSphere Servers might not   generate property collector update notifications for this property.   To obtain the latest value of the property, you can use   PropertyCollector methods RetrievePropertiesEx or WaitForUpdatesEx.   If you use the PropertyCollector.WaitForUpdatesEx method, specify   an empty string for the version parameter. Any other version value will not   produce any property values as no updates are generated. |
| <a href='config'>config</a> | [vim.host.ConfigInfo](vim.host.ConfigInfo.md "vim.host.ConfigInfo") | true | None | Host configuration information.  This might not be available for a disconnected   host. |
| <a href='vm'>vm</a> | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | true | None | List of virtual machines associated with this host. |
| <a href='datastore'>datastore</a> | [vim.Datastore](vim.Datastore.md "vim.Datastore") | true | System.View | A collection of references to the subset of datastore objects in the datacenter   that are available in this HostSystem. |
| <a href='network'>network</a> | [vim.Network](vim.Network.md "vim.Network") | true | System.View | A collection of references to the subset of network objects in the datacenter that   are available in this HostSystem. |
| <a href='datastoreBrowser'>datastoreBrowser</a> | [vim.host.DatastoreBrowser](vim.host.DatastoreBrowser.md "vim.host.DatastoreBrowser") | None | System.View | DatastoreBrowser to browse datastores for this host. |
| <a href='systemResources'>systemResources</a> | [vim.host.SystemResourceInfo](vim.host.SystemResourceInfo.md "vim.host.SystemResourceInfo") | true | None | Reference for the system resource hierarchy, used for configuring the set of   resources reserved to the system and unavailable to virtual machines. |


QueryTpmAttestationReport()
---------------------------

| service name | QueryTpmAttestationReport |
|:--|:--|
| since version | [vSphere API 5.1](vim.version.md#None) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




QueryHostConnectionInfo()
-------------------------

| service name | QueryHostConnectionInfo |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




UpdateSystemResources([resourceInfo](vim.host.SystemResourceInfo.md "vim.host.SystemResourceInfo"))
---------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | UpdateSystemResources |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Resources |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the resource specification is invalid. |




UpdateSystemSwapConfiguration([sysSwapConfig](vim.host.SystemSwapConfiguration.md "vim.host.SystemSwapConfiguration"))
----------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | UpdateSystemSwapConfiguration |
|:--|:--|
| since version | [vSphere API 5.1](vim.version.md#None) |
| privilege    | Host.Config.Settings |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the supplied sysSwapConfig is not correct.<br>See <a href="vim.host.SystemSwapConfiguration.md">HostSystemSwapConfiguration</a><br> |




ReconnectHost([cnxSpec](vim.host.ConnectSpec.md "vim.host.ConnectSpec"), [reconnectSpec](vim.HostSystem.ReconnectSpec.md "vim.HostSystem.ReconnectSpec"))
---------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.HostConnectFault](vim.fault.HostConnectFault.md "vim.fault.HostConnectFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.NoHost](vim.fault.NoHost.md "vim.fault.NoHost"), [vim.fault.AlreadyBeingManaged](vim.fault.AlreadyBeingManaged.md "vim.fault.AlreadyBeingManaged"), [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.NotSupportedHost](vim.fault.NotSupportedHost.md "vim.fault.NotSupportedHost"), [vmodl.fault.NotEnoughLicenses](vmodl.fault.NotEnoughLicenses.md "vmodl.fault.NotEnoughLicenses"), [vim.fault.SSLVerifyFault](vim.fault.SSLVerifyFault.md "vim.fault.SSLVerifyFault")

---
| service name | ReconnectHost |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Connection |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin") | if the method fails to authenticate with the host. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the host is not disconnected. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the host name is invalid. |
| [vim.fault.HostConnectFault](vim.fault.HostConnectFault.md "vim.fault.HostConnectFault") | if an error occurred when attempting to reconnect 		      to a host. Typically, a more specific subclass, such as 		      AlreadyBeingManaged, is thrown. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if no host can be added to this group. This is the case if           the ComputeResource is a standalone type. |
| [vim.fault.AlreadyBeingManaged](vim.fault.AlreadyBeingManaged.md "vim.fault.AlreadyBeingManaged") | if host is already being managed by another           VirtualCenter server |
| [vmodl.fault.NotEnoughLicenses](vmodl.fault.NotEnoughLicenses.md "vmodl.fault.NotEnoughLicenses") | if there are not enough licenses to add this host. |
| [vim.fault.NoHost](vim.fault.NoHost.md "vim.fault.NoHost") | if the method is unable to contact the server. |
| [vim.fault.NotSupportedHost](vim.fault.NotSupportedHost.md "vim.fault.NotSupportedHost") | if the host is running a software version that is not                           supported. |
| [vim.fault.SSLVerifyFault](vim.fault.SSLVerifyFault.md "vim.fault.SSLVerifyFault") | if the host certificate could not be authenticated. |




DisconnectHost()
----------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | DisconnectHost |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Connection |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if run directly on an ESX Server host. |




EnterMaintenanceMode([maintenanceSpec](vim.host.MaintenanceSpec.md "vim.host.MaintenanceSpec"))
-----------------------------------------------------------------------------------------------
 raises [vim.fault.Timedout](vim.fault.Timedout.md "vim.fault.Timedout"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled")

---
| service name | EnterMaintenanceMode |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Maintenance |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the host is already in maintenance mode. |
| [vim.fault.Timedout](vim.fault.Timedout.md "vim.fault.Timedout") | if the operation timed out. |
| [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled") | if the operation is canceled. |




ExitMaintenanceMode()
---------------------
 raises [vim.fault.Timedout](vim.fault.Timedout.md "vim.fault.Timedout"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | ExitMaintenanceMode |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Maintenance |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the host is not in maintenance mode. |
| [vim.fault.Timedout](vim.fault.Timedout.md "vim.fault.Timedout") | vim.fault.Timedout |




RebootHost()
------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | RebootHost |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Maintenance |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if "force" is false and the host is not in maintenance mode. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host does not support the reboot operation. |




ShutdownHost()
--------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | ShutdownHost |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Maintenance |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if "force" is false and the host is not in                         maintenance mode. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host does not support shutdown. |




PowerDownHostToStandBy()
------------------------
 raises [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled"), [vim.fault.HostPowerOpFailed](vim.fault.HostPowerOpFailed.md "vim.fault.HostPowerOpFailed"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.Timedout](vim.fault.Timedout.md "vim.fault.Timedout")

---
| service name | PowerDownHostToStandBy |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | Host.Config.Maintenance |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostPowerOpFailed](vim.fault.HostPowerOpFailed.md "vim.fault.HostPowerOpFailed") | if the standby operation fails. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the host is already in standby mode, or disconnected. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host does not support standby mode. |
| [vim.fault.Timedout](vim.fault.Timedout.md "vim.fault.Timedout") | vim.fault.Timedout |
| [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled") | if the operation is canceled. |




PowerUpHostFromStandBy()
------------------------
 raises [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled"), [vim.fault.HostPowerOpFailed](vim.fault.HostPowerOpFailed.md "vim.fault.HostPowerOpFailed"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.Timedout](vim.fault.Timedout.md "vim.fault.Timedout")

---
| service name | PowerUpHostFromStandBy |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | Host.Config.Maintenance |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostPowerOpFailed](vim.fault.HostPowerOpFailed.md "vim.fault.HostPowerOpFailed") | if the standby operation fails. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the host is in a state from which it          cannot be woken up (e.g., disconnected, poweredOff) |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host does not support standby mode. |
| [vim.fault.Timedout](vim.fault.Timedout.md "vim.fault.Timedout") | vim.fault.Timedout |
| [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled") | if the operation is canceled. |




QueryMemoryOverhead()
---------------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
### Deprecated
As of VI API 2.5, use <a href="vim.HostSystem.md#queryOverheadEx">QueryMemoryOverheadEx</a>.

| service name | QueryMemoryOverhead |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.Read |
| return type | None |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host does not have memory resource allocation   features. |




QueryMemoryOverheadEx([vmConfigInfo](vim.vm.ConfigInfo.md "vim.vm.ConfigInfo"))
-------------------------------------------------------------------------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
### Deprecated
As of VI API 5.5, use   <a href="vim.vm.ConfigInfo.md#initialOverhead">initialOverhead</a>.

| service name | QueryMemoryOverheadEx |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | System.Read |
| return type | None |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host does not have memory resource allocation   features. |




ReconfigureHostForDAS()
-----------------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.DasConfigFault](vim.fault.DasConfigFault.md "vim.fault.DasConfigFault")

---
| service name | ReconfigureHostForDAS |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Connection |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DasConfigFault](vim.fault.DasConfigFault.md "vim.fault.DasConfigFault") | if there is a problem reconfiguring the host for HA. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if run directly on an ESX Server host. |




UpdateFlags([flagInfo](vim.host.FlagInfo.md "vim.host.FlagInfo"))
-----------------------------------------------------------------

| service name | UpdateFlags |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | Host.Config.Settings |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




EnterLockdownMode()
-------------------
 raises [vim.fault.DisableAdminNotSupported](vim.fault.DisableAdminNotSupported.md "vim.fault.DisableAdminNotSupported"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.AdminDisabled](vim.fault.AdminDisabled.md "vim.fault.AdminDisabled")

---
| service name | EnterLockdownMode |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#None) |
| privilege    | Host.Config.Settings |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | <br>See <a href="vim.AuthorizationManager.md">AuthorizationManager</a><br> |
| [vim.fault.AdminDisabled](vim.fault.AdminDisabled.md "vim.fault.AdminDisabled") | If the host's Administrator permission has been                          disabled.<br>See <a href="vim.AuthorizationManager.md">AuthorizationManager</a><br> |
| [vim.fault.DisableAdminNotSupported](vim.fault.DisableAdminNotSupported.md "vim.fault.DisableAdminNotSupported") | If invoked directly on the host or the                          host doesn't support this operation.<br>See <a href="vim.AuthorizationManager.md">AuthorizationManager</a><br> |




ExitLockdownMode()
------------------
 raises [vim.fault.DisableAdminNotSupported](vim.fault.DisableAdminNotSupported.md "vim.fault.DisableAdminNotSupported"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.AdminNotDisabled](vim.fault.AdminNotDisabled.md "vim.fault.AdminNotDisabled")

---
| service name | ExitLockdownMode |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#None) |
| privilege    | Host.Config.Settings |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | <br>See <a href="vim.AuthorizationManager.md">AuthorizationManager</a><br> |
| [vim.fault.DisableAdminNotSupported](vim.fault.DisableAdminNotSupported.md "vim.fault.DisableAdminNotSupported") | If invoked directly on the host or the                                      host doesn't support this operation.<br>See <a href="vim.AuthorizationManager.md">AuthorizationManager</a><br> |
| [vim.fault.AdminNotDisabled](vim.fault.AdminNotDisabled.md "vim.fault.AdminNotDisabled") | If the host's Administrator permission                                      is not disabled.<br>See <a href="vim.AuthorizationManager.md">AuthorizationManager</a><br> |




AcquireCimServicesTicket()
--------------------------

| service name | AcquireCimServicesTicket |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | Host.Cim.CimInteraction |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




UpdateIpmi([ipmiInfo](vim.host.IpmiInfo.md "vim.host.IpmiInfo"))
----------------------------------------------------------------
 raises [vim.fault.InvalidIpmiLoginInfo](vim.fault.InvalidIpmiLoginInfo.md "vim.fault.InvalidIpmiLoginInfo"), [vim.fault.InvalidIpmiMacAddress](vim.fault.InvalidIpmiMacAddress.md "vim.fault.InvalidIpmiMacAddress")

---
| service name | UpdateIpmi |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Host.Config.Settings |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidIpmiLoginInfo](vim.fault.InvalidIpmiLoginInfo.md "vim.fault.InvalidIpmiLoginInfo") | if the supplied user ID and/or password is invalid. |
| [vim.fault.InvalidIpmiMacAddress](vim.fault.InvalidIpmiMacAddress.md "vim.fault.InvalidIpmiMacAddress") | if the supplied MAC address is invalid. |




RetrieveHardwareUptime()
------------------------

| service name | RetrieveHardwareUptime |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#None) |
| privilege    | System.Read |
| return type | None |
### Faults
| fault | description |
|:------|:------------|




