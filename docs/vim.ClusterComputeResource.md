vim.ClusterComputeResource
==========================
inherits from [vim.ComputeResource](vim.ComputeResource.md "vim.ComputeResource")


The <a href="vim.ClusterComputeResource.md">ClusterComputeResource</a> data object aggregates the compute   resources of associated <a href="vim.HostSystem.md">HostSystem</a> objects into a single   compute resource for use by virtual machines. The cluster services   such as HA (High Availability), DRS (Distributed Resource Scheduling),   and EVC (Enhanced vMotion Compatibility), enhance the utility of this   single compute resource.   <p>   Use the <a href="vim.Folder.md">Folder</a>.<a href="vim.Folder.md#createClusterEx">CreateClusterEx</a> method   to create an instance of this object.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='configuration'>configuration</a> | [vim.cluster.ConfigInfo](vim.cluster.ConfigInfo.md "vim.cluster.ConfigInfo") | None | None | Configuration of the cluster. |
| <a href='recommendation'>recommendation</a> | [vim.cluster.Recommendation](vim.cluster.Recommendation.md "vim.cluster.Recommendation") | true | System.Read | List of recommended actions for the cluster. It is   possible that the current set of recommendations may be empty,   either due to not having any running dynamic recommendation   generation module, or since there may be no recommended actions   at this time. |
| <a href='drsRecommendation'>drsRecommendation</a> | [vim.cluster.DrsRecommendation](vim.cluster.DrsRecommendation.md "vim.cluster.DrsRecommendation") | true | None | If DRS is enabled, this returns the set of recommended   migrations from the DRS module. The current set of   recommendations may be empty, since there may be no recommended   migrations at this time, or it is possible that DRS is not   enabled. |
| <a href='migrationHistory'>migrationHistory</a> | [vim.cluster.DrsMigration](vim.cluster.DrsMigration.md "vim.cluster.DrsMigration") | true | None | The set of migration decisions that have recently been performed.   <p>   This list is populated only when DRS is in automatic mode. |
| <a href='actionHistory'>actionHistory</a> | [vim.cluster.ActionHistory](vim.cluster.ActionHistory.md "vim.cluster.ActionHistory") | true | None | The set of actions that have been performed recently. |
| <a href='drsFault'>drsFault</a> | [vim.cluster.DrsFaults](vim.cluster.DrsFaults.md "vim.cluster.DrsFaults") | true | System.Read | A collection of the DRS faults generated in the last DRS invocation.   Each element of the collection is the set of faults generated in one   recommendation.    DRS faults are generated when DRS tries to make recommendations   for rule enforcement, power management, etc., and indexed in a tree   structure with reason for recommendations and VM to migrate (optional)   as the index keys.    In releases after vSphere API 5.0, vSphere Servers might not   generate property collector update notifications for this property.   To obtain the latest value of the property, you can use   PropertyCollector methods RetrievePropertiesEx or WaitForUpdatesEx.   If you use the PropertyCollector.WaitForUpdatesEx method, specify   an empty string for the version parameter. Any other version value will not   produce any property values as no updates are generated. |


ReconfigureCluster([spec](vim.cluster.ConfigSpec.md "vim.cluster.ConfigSpec"))
------------------------------------------------------------------------------
 raises [vim.fault.CannotDisableDrsOnClustersWithVApps](vim.fault.CannotDisableDrsOnClustersWithVApps.md "vim.fault.CannotDisableDrsOnClustersWithVApps")

---
### Deprecated
As of VI API 2.5, use <a href="vim.ComputeResource.md#reconfigureEx">ReconfigureComputeResource_Task</a>.

| service name | ReconfigureCluster |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Inventory.EditCluster |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.CannotDisableDrsOnClustersWithVApps](vim.fault.CannotDisableDrsOnClustersWithVApps.md "vim.fault.CannotDisableDrsOnClustersWithVApps") | If DRS is being disabled and the                                               cluster contains one or more vApps. |




ApplyRecommendation([key](#string "string"))
--------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | ApplyRecommendation |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | dynamic |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If the specified key refers to a non-existent or an                           already executed recommendation. |




CancelRecommendation([key](#string "string"))
---------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | CancelRecommendation |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#None) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If the specified key refers to a non-existent or an                           already executed recommendation. |




RecommendHostsForVm([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [pool](vim.ResourcePool.md "vim.ResourcePool"))
---------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
### Deprecated
As of VI API 2.5, use <a href="vim.Datacenter.md#powerOnVm">PowerOnMultiVM_Task</a>.   <a href="vim.ClusterComputeResource.md#recommendHostsForVm">RecommendHostsForVm</a> cannot make  any recommendations if DRS cannot   find the specified host in the cluster.   With <a href="vim.Datacenter.md#powerOnVm">PowerOnMultiVM_Task</a>, DRS attempts to migrate virtual machines   and power on hosts in standby mode, given the same conditions.   <p>

| service name | RecommendHostsForVm |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if DRS is not enabled. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the virtual machine is powered on and the optional            ResourcePool argument is either not specified or is in the same cluster            as the virtual machine. |




AddHost([spec](vim.host.ConnectSpec.md "vim.host.ConnectSpec"), [resourcePool](vim.ResourcePool.md "vim.ResourcePool"), [license](#string "string"))
----------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.AgentInstallFailed](vim.fault.AgentInstallFailed.md "vim.fault.AgentInstallFailed"), [vim.fault.TooManyHosts](vim.fault.TooManyHosts.md "vim.fault.TooManyHosts"), [vim.fault.HostConnectFault](vim.fault.HostConnectFault.md "vim.fault.HostConnectFault"), [vim.fault.NoHost](vim.fault.NoHost.md "vim.fault.NoHost"), [vim.fault.AlreadyBeingManaged](vim.fault.AlreadyBeingManaged.md "vim.fault.AlreadyBeingManaged"), [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vim.fault.AlreadyConnected](vim.fault.AlreadyConnected.md "vim.fault.AlreadyConnected"), [vim.fault.NotSupportedHost](vim.fault.NotSupportedHost.md "vim.fault.NotSupportedHost"), [vmodl.fault.NotEnoughLicenses](vmodl.fault.NotEnoughLicenses.md "vmodl.fault.NotEnoughLicenses"), [vim.fault.SSLVerifyFault](vim.fault.SSLVerifyFault.md "vim.fault.SSLVerifyFault")

---
| service name | AddHost |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Inventory.AddHostToCluster |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin") | if "asConnected" is specified but authentication with the           new host fails. |
| [vim.fault.HostConnectFault](vim.fault.HostConnectFault.md "vim.fault.HostConnectFault") | if an error occurred when connecting to a host. 		   Typically, a more specific subclass, such as AlreadyBeingManaged, 		   is thrown. |
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if another host in the same cluster has the name. |
| [vim.fault.AlreadyBeingManaged](vim.fault.AlreadyBeingManaged.md "vim.fault.AlreadyBeingManaged") | if the host is already being managed by a           VirtualCenter server. |
| [vmodl.fault.NotEnoughLicenses](vmodl.fault.NotEnoughLicenses.md "vmodl.fault.NotEnoughLicenses") | if no licenses are available to add this host. |
| [vim.fault.NoHost](vim.fault.NoHost.md "vim.fault.NoHost") | if the host cannot be contacted. |
| [vim.fault.NotSupportedHost](vim.fault.NotSupportedHost.md "vim.fault.NotSupportedHost") | if the host is running a software version that does           not support clustering features. It may still be possible to add           the host as a stand-alone host. |
| [vim.fault.TooManyHosts](vim.fault.TooManyHosts.md "vim.fault.TooManyHosts") | if no additional hosts can be added to the cluster. |
| [vim.fault.AgentInstallFailed](vim.fault.AgentInstallFailed.md "vim.fault.AgentInstallFailed") | if there is an error installing the VirtualCenter agent           on the host. |
| [vim.fault.AlreadyConnected](vim.fault.AlreadyConnected.md "vim.fault.AlreadyConnected") | if asConnected is true and the host is already           connected to VirtualCenter. |
| [vim.fault.SSLVerifyFault](vim.fault.SSLVerifyFault.md "vim.fault.SSLVerifyFault") | if the host certificate could not be authenticated |




MoveInto([host](vim.HostSystem.md "vim.HostSystem"))
----------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vim.fault.TooManyHosts](vim.fault.TooManyHosts.md "vim.fault.TooManyHosts"), [vim.fault.DisallowedOperationOnFailoverHost](vim.fault.DisallowedOperationOnFailoverHost.md "vim.fault.DisallowedOperationOnFailoverHost")

---
| service name | MoveInto |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Inventory.EditCluster |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if the host is already in the cluster |
| [vim.fault.TooManyHosts](vim.fault.TooManyHosts.md "vim.fault.TooManyHosts") | if no additional hosts can be added to the cluster. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if a host is already part of a cluster and is not in           maintenance mode. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if one of the hosts is not part of the same datacenter           as the cluster. |
| [vim.fault.DisallowedOperationOnFailoverHost](vim.fault.DisallowedOperationOnFailoverHost.md "vim.fault.DisallowedOperationOnFailoverHost") | if the host is being moved           from a cluster and was configured as a failover host in that           cluster. See <a href="vim.cluster.FailoverHostAdmissionControlPolicy.md">ClusterFailoverHostAdmissionControlPolicy</a>. |




MoveHostInto([host](vim.HostSystem.md "vim.HostSystem"), [resourcePool](vim.ResourcePool.md "vim.ResourcePool"))
----------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TooManyHosts](vim.fault.TooManyHosts.md "vim.fault.TooManyHosts")

---
| service name | MoveHostInto |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Inventory.EditCluster |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TooManyHosts](vim.fault.TooManyHosts.md "vim.fault.TooManyHosts") | if no additional hosts can be added to the cluster. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if a host is already part of a cluster and is not in           maintenance mode. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the host is not a part of the same datacenter as           the cluster or if the specified resource pool is not part of the cluster           or if the source and destination clusters are the same. |




RefreshRecommendation()
-----------------------

| service name | RefreshRecommendation |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | Host.Inventory.EditCluster |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




RetrieveDasAdvancedRuntimeInfo()
--------------------------------

| service name | RetrieveDasAdvancedRuntimeInfo |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




ClusterEnterMaintenanceMode([host](vim.HostSystem.md "vim.HostSystem"), [option](vim.option.OptionValue.md "vim.option.OptionValue"))
-------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | ClusterEnterMaintenanceMode |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | for unknown option keys or bad values. |




