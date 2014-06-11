vim.Datacenter
==============
inherits from [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity")


The <a href="vim.Datacenter.md">Datacenter</a> managed object provides the interface to the common container   object for hosts, virtual machines, networks, and datastores. These entities   must be under a distinct datacenter in the inventory, and datacenters may not   be nested under other datacenters.   <p>   Every <a href="vim.Datacenter.md">Datacenter</a> has the following set of dedicated folders. These folders are empty   until you create entities for the Datacenter.   <ul>       <li> A folder for <a href="vim.VirtualMachine.md">VirtualMachine</a>, template, and            <a href="vim.VirtualApp.md">VirtualApp</a> objects.       <li> A folder for a <a href="vim.ComputeResource.md">ComputeResource</a> hierarchy.       <li> A folder for <a href="vim.Network.md">Network</a>, <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>,            and <a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a> objects.       <li> A folder for <a href="vim.Datastore.md">Datastore</a> objects.   </ul>   <p>   For a visual representation of the organization of objects in a vCenter   hierarchy, see the description of the <a href="vim.ServiceInstance.md">ServiceInstance</a> object.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='vmFolder'>vmFolder</a> | [vim.Folder](vim.Folder.md "vim.Folder") | None | System.View | A reference to the folder hierarchy that contains <a href="vim.VirtualMachine.md">VirtualMachine</a>    virtual machine templates (identified by the <a href="vim.vm.ConfigInfo.md#template">template</a>   property, and <a href="vim.VirtualApp.md">VirtualApp</a> objects for this datacenter.   <p>     Note that a VirtualApp that is a child of a <a href="vim.ResourcePool.md">ResourcePool</a>   may also be visible in this folder. VirtualApp objects can be nested,    but only the parent VirtualApp can be visible in the folder.   <p>   This folder is guaranteed to exist. |
| <a href='hostFolder'>hostFolder</a> | [vim.Folder](vim.Folder.md "vim.Folder") | None | System.View | A reference to the folder hierarchy that contains   the compute resources, including hosts and clusters, for this datacenter.   <p>   This folder is guaranteed to exist. |
| <a href='datastoreFolder'>datastoreFolder</a> | [vim.Folder](vim.Folder.md "vim.Folder") | None | System.View | A reference to the folder hierarchy that contains   the datastores for this datacenter.   <p>   This folder is guaranteed to exist. |
| <a href='networkFolder'>networkFolder</a> | [vim.Folder](vim.Folder.md "vim.Folder") | None | System.View | A reference to the folder hierarchy that contains the network entities   for this datacenter. The folder can include <a href="vim.Network.md">Network</a>,    <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>, and    <a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a> objects.   <p>   This folder is guaranteed to exist. |
| <a href='datastore'>datastore</a> | [vim.Datastore](vim.Datastore.md "vim.Datastore") | true | None | A collection of references to the datastore objects   available in this datacenter. |
| <a href='network'>network</a> | [vim.Network](vim.Network.md "vim.Network") | true | None | A collection of references to the network objects   available in this datacenter. |
| <a href='configuration'>configuration</a> | [vim.Datacenter.ConfigInfo](vim.Datacenter.ConfigInfo.md "vim.Datacenter.ConfigInfo") | None | System.View | Configuration of the datacenter. |


QueryConnectionInfo([hostname](#string "string"), [username](#string "string"), [password](#string "string"), [sslThumbprint](#string "string"))
------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.HostConnectFault](vim.fault.HostConnectFault.md "vim.fault.HostConnectFault"), [vim.fault.NoHost](vim.fault.NoHost.md "vim.fault.NoHost"), [vim.fault.SSLDisabledFault](vim.fault.SSLDisabledFault.md "vim.fault.SSLDisabledFault"), [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.AlreadyConnected](vim.fault.AlreadyConnected.md "vim.fault.AlreadyConnected"), [vim.fault.NotSupportedHost](vim.fault.NotSupportedHost.md "vim.fault.NotSupportedHost"), [vim.fault.SSLVerifyFault](vim.fault.SSLVerifyFault.md "vim.fault.SSLVerifyFault")

---
| service name | QueryConnectionInfo |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin") | if unable to authenticate with the host. |
| [vim.fault.HostConnectFault](vim.fault.HostConnectFault.md "vim.fault.HostConnectFault") | if an error occurred when querying about a host.           Typically, a more specific subclass, such as AlreadyBeingManaged, 		   is thrown. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if called directly on a host. |
| [vim.fault.NoHost](vim.fault.NoHost.md "vim.fault.NoHost") | if unable to contact the host. |
| [vim.fault.NotSupportedHost](vim.fault.NotSupportedHost.md "vim.fault.NotSupportedHost") | if the software version on the host is not supported. |
| [vim.fault.AlreadyConnected](vim.fault.AlreadyConnected.md "vim.fault.AlreadyConnected") | if the host is already being managed by this server. |
| [vim.fault.SSLDisabledFault](vim.fault.SSLDisabledFault.md "vim.fault.SSLDisabledFault") | if the host has ssl access disabled |
| [vim.fault.SSLVerifyFault](vim.fault.SSLVerifyFault.md "vim.fault.SSLVerifyFault") | if the host certificate could not be authenticated |




PowerOnMultiVM([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [option](vim.option.OptionValue.md "vim.option.OptionValue"))
------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | PowerOnMultiVM |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | System.View |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | for unknown option keys or bad values. |




queryDatacenterConfigOptionDescriptor()
---------------------------------------

| service name | queryDatacenterConfigOptionDescriptor |
|:--|:--|
| since version | [vSphere API 5.1](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




ReconfigureDatacenter([spec](vim.Datacenter.ConfigSpec.md "vim.Datacenter.ConfigSpec"))
---------------------------------------------------------------------------------------

| service name | ReconfigureDatacenter |
|:--|:--|
| since version | [vSphere API 5.1](vim.version.md#None) |
| privilege    | Datacenter.Reconfigure |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|




