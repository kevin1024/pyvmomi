vim.ComputeResource
===================
inherits from [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity")


Represents a set of physical compute resources for a set of virtual machines.   <p>   The base type <a href="vim.ComputeResource.md">ComputeResource</a>, when instantiated by calling   <a href="vim.Folder.md#addStandaloneHost">AddStandaloneHost_Task</a>, represents a single host. The subclass   <a href="vim.ClusterComputeResource.md">ClusterComputeResource</a> represents a cluster of hosts and adds distributed management   features such as availability and resource scheduling.   <p>   A <a href="vim.ComputeResource.md">ComputeResource</a> always has a root <a href="vim.ResourcePool.md">ResourcePool</a> associated with it.   Certain types of  clusters such as those with VMware DRS enabled and standalone hosts   (ESX Server 3) support the creation of <a href="vim.ResourcePool.md">ResourcePool</a> hierarchies.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='resourcePool'>resourcePool</a> | [vim.ResourcePool](vim.ResourcePool.md "vim.ResourcePool") | true | System.View | Reference to root resource pool. |
| <a href='host'>host</a> | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | true | System.View | List of hosts that are part of this compute resource. If the compute resource is a   standalone type, then this list contains just one element. |
| <a href='datastore'>datastore</a> | [vim.Datastore](vim.Datastore.md "vim.Datastore") | true | System.View | The datastore property is the subset of datastore objects in the datacenter   available in this ComputeResource.   <p>   This property is computed as the aggregate set of datastores available from all   the hosts that are part of this compute resource. |
| <a href='network'>network</a> | [vim.Network](vim.Network.md "vim.Network") | true | System.View | The subset of network objects available in the datacenter that is available in   this ComputeResource.   <p>   This property is computed as the aggregate set of networks available from all the   hosts that are part of this compute resource. |
| <a href='summary'>summary</a> | [vim.ComputeResource.Summary](vim.ComputeResource.Summary.md "vim.ComputeResource.Summary") | None | None | Basic runtime information about a compute resource. This information is used on   summary screens and in list views. |
| <a href='environmentBrowser'>environmentBrowser</a> | [vim.EnvironmentBrowser](vim.EnvironmentBrowser.md "vim.EnvironmentBrowser") | true | System.View | The environment browser object that identifies the environments that are supported   on this compute resource. |
| <a href='configurationEx'>configurationEx</a> | [vim.ComputeResource.ConfigInfo](vim.ComputeResource.ConfigInfo.md "vim.ComputeResource.ConfigInfo") | None | None | Configuration of the compute resource; applies to both standalone hosts   and clusters. For a cluster this property will return a   <a href="vim.cluster.ConfigInfoEx.md">ClusterConfigInfoEx</a> object. |


ReconfigureComputeResource([spec](vim.ComputeResource.ConfigSpec.md "vim.ComputeResource.ConfigSpec"))
------------------------------------------------------------------------------------------------------
 raises [vim.fault.CannotDisableDrsOnClustersWithVApps](vim.fault.CannotDisableDrsOnClustersWithVApps.md "vim.fault.CannotDisableDrsOnClustersWithVApps")

---
| service name | ReconfigureComputeResource |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | Host.Inventory.EditCluster |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.CannotDisableDrsOnClustersWithVApps](vim.fault.CannotDisableDrsOnClustersWithVApps.md "vim.fault.CannotDisableDrsOnClustersWithVApps") | If DRS is being disabled and the                                               cluster contains one or more vApps. |




