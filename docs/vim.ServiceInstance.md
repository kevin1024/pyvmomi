vim.ServiceInstance
===================


The <a href="vim.ServiceInstance.md">ServiceInstance</a> managed object is the singleton root object of the inventory   on both vCenter servers and servers running on standalone host agents.   The server creates the <a href="vim.ServiceInstance.md">ServiceInstance</a> automatically, and also automatically   creates the various manager entities that provide services in the virtual   environment. Some examples of manager entities are <a href="vim.LicenseManager.md">LicenseManager</a>,   <a href="vim.PerformanceManager.md">PerformanceManager</a>, and <a href="vim.view.ViewManager.md">ViewManager</a>. You can   access the manager entities through the <a href="vim.ServiceInstance.md#content">content</a> property.   <p>   A vSphere API client application begins by connecting to a server   and obtaining a reference to the <a href="vim.ServiceInstance.md">ServiceInstance</a>. The client can then use   the <a href="vim.ServiceInstance.md#retrieveContent">RetrieveServiceContent</a> method to gain   access to the various vSphere manager entities and to the root folder   of the inventory.    <p>   When you create managed objects, the server adds them to the inventory.   The inventory of managed objects includes instances the following object types:    <ul>     <li><a href="vim.ServiceInstance.md">ServiceInstance</a>  -- Root of the inventory; created by vSphere.     <li><a href="vim.Datacenter.md">Datacenter</a>       -- A container that represents a virtual                                         data center. It contains hosts, network entities,                                         virtual machines and virtual applications,                                         and datastores.     <li><a href="vim.Folder.md">Folder</a>           -- A container used for hierarchical                                         organization of the inventory.     <li><a href="vim.VirtualMachine.md">VirtualMachine</a>   -- A virtual machine.     <li><a href="vim.VirtualApp.md">VirtualApp</a>       -- A virtual application.     <li><a href="vim.ComputeResource.md">ComputeResource</a>  -- A compute resource                           (either a cluster or a stand-alone host).     <li><a href="vim.ResourcePool.md">ResourcePool</a>     -- A subset of resources provided by a ComputeResource.     <li><a href="vim.HostSystem.md">HostSystem</a>       -- A single host (ESX Server or VMware Server).     <li><a href="vim.Network.md">Network</a>          -- A network available to either hosts or virtual                                         machines.     <li><a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a> -- A distributed virtual switch.     <li><a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a> -- A distributed virtual port group.     <li><a href="vim.Datastore.md">Datastore</a>        -- Platform-independent, host-independent storage                                         for virtual machine files.   </ul>   <p>   The following figure shows the organization of managed objects in the   vCenter hierarchy:   <p><img src="vc_si_hierarchy.gif" alt="vCenter ServiceInstance Hierarchy"/>   <p>   Every Datacenter has the following set of dedicated folders.    These folders are empty until you create entities for the Datacenter.   <ul>       <li> A folder for any combination of <a href="vim.VirtualMachine.md">VirtualMachine</a>            and/or <a href="vim.VirtualApp.md">VirtualApp</a> objects. <a href="vim.VirtualApp.md">VirtualApp</a> objects can be nested,             but only the parent <a href="vim.VirtualApp.md">VirtualApp</a> can be visible in the folder.            Virtual machines that are children of virtual applications are not            associated with a VirtualMachine/VirtualApp folder.       <li> A folder for a <a href="vim.ComputeResource.md">ComputeResource</a> hierarchy.       <li> A folder for network entities - any combination            of <a href="vim.Network.md">Network</a>, <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>, and/or            <a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a> objects.       <li> A folder for <a href="vim.Datastore.md">Datastore</a> objects.   </ul>   <p>   The host agent hierarchy has the same general form as the vCenter hierarchy,   but most of the objects are limited to one instance:   <p><img src="ha_si_hierarchy.gif" alt="Host Agent Service Instance Hierarchy"/>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='serverClock'>serverClock</a> | datetime | None | System.View | Contains the time most recently obtained from the server.   The time is not necessarily current. This property is intended for use   with the PropertyCollector <a href="vmodl.query.PropertyCollector.md#waitForUpdates">WaitForUpdates</a>   method. The PropertyCollector will provide notification if some event occurs   that changes the server clock time in a non-linear fashion.   <p>   You should not rely on the serverClock property to get the current time   on the server; instead, use the <a href="vim.ServiceInstance.md#currentTime">CurrentTime</a> method. |
| <a href='capability'>capability</a> | [vim.Capability](vim.Capability.md "vim.Capability") | None | System.View | API-wide capabilities. |
| <a href='content'>content</a> | [vim.ServiceInstanceContent](vim.ServiceInstanceContent.md "vim.ServiceInstanceContent") | None | System.Anonymous | The properties of the ServiceInstance managed object. The content property   is identical to the return value from the   <a href="vim.ServiceInstance.md#retrieveContent">RetrieveServiceContent</a> method.   <p>   Use the content property with the <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a>   to perform inventory traversal that includes the ServiceInstance.   (In the absence of a content property, a traversal that encounters   the <a href="vim.ServiceInstance.md">ServiceInstance</a> would require calling   the <a href="vim.ServiceInstance.md#retrieveContent">RetrieveServiceContent</a> method,   and then invoking a second traversal to continue.) |


CurrentTime()
-------------

| service name | CurrentTime |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type | [datetime](datetime.md "datetime") |
### Faults
| fault | description |
|:------|:------------|




RetrieveServiceContent()
------------------------

| service name | RetrieveServiceContent |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.Anonymous |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




ValidateMigration([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [state](vim.VirtualMachine.PowerState.md "vim.VirtualMachine.PowerState"), [testType](#string "string"), [pool](vim.ResourcePool.md "vim.ResourcePool"), [host](vim.HostSystem.md "vim.HostSystem"))
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.NoActiveHostInCluster](vim.fault.NoActiveHostInCluster.md "vim.fault.NoActiveHostInCluster"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
### Deprecated
As of vSphere API 4.0, use <a href="vim.vm.check.ProvisioningChecker.md">VirtualMachineProvisioningChecker</a>  instead.

| service name | ValidateMigration |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | vim.fault.InvalidState |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the target host(s) and target pool for a          migration are not associated with the same compute resource,          or if the host parameter is left unset when the target pool is          associated with a non-DRS cluster. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the state argument is set and at least one          of the specified virtual machines is not in that power state. |
| [vim.fault.NoActiveHostInCluster](vim.fault.NoActiveHostInCluster.md "vim.fault.NoActiveHostInCluster") | if a target host is not specified and a          cluster associated with a target pool does not contain at least one          potential target host. A host must be connected and not in maintenance          mode in order to be considered as a potential target host. |




QueryVMotionCompatibility([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [host](vim.HostSystem.md "vim.HostSystem"), [compatibility](#string "string"))
----------------------------------------------------------------------------------------------------------------------------------------------------------

### Deprecated
As of vSphere API 4.0, use   <a href="vim.vm.check.ProvisioningChecker.md#queryVMotionCompatibilityEx">QueryVMotionCompatibilityEx_Task</a> instead.

| service name | QueryVMotionCompatibility |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Resource.QueryVMotion |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




RetrieveProductComponents()
---------------------------

| service name | RetrieveProductComponents |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | System.Anonymous |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




