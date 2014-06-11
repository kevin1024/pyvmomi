vim.PerformanceManager
======================


This managed object type provides the service interface for obtaining   statistical data about various aspects of system performance, as generated   and maintained by the system's performance providers. A "performance   provider" (<a href="vim.PerformanceManager.ProviderSummary.md">PerfProviderSummary</a>) is any managed object   that generates utilization or other performance metrics. Performance   providers include <a href="vim.ManagedEntity.md">managed entities</a>, such as <a href="vim.HostSystem.md">hosts</a>, <a href="vim.VirtualMachine.md">virtual machines</a>, <a href="vim.ComputeResource.md">compute resources</a>, <a href="vim.ResourcePool.md">resource   pools</a>, <a href="vim.Datastore.md">datastores</a>, and <a href="vim.Network.md">networks</a>.   Performance providers also include physical or virtual devices associated   with these objects, such as virtual host-bus adapters and network-interface   controllers (NICs)    <p> <a name="counterTables"></a><b>Performance Counters</b> <br/> Each   performance provider&#151;the instrumented device or entity&#151;has its own   set of <a href="vim.PerformanceManager.CounterInfo.md">counters</a> that provides   metadata about its available <a href="vim.PerformanceManager.EntityMetric.md">metrics</a>. Each counter has a unique <a href="vim.PerformanceManager.CounterInfo.md#key">key</a>, referred to as the counterId. The   actual performance metrics generated at runtime are identified by this   <a href="vim.PerformanceManager.MetricId.md#counterId">counterId</a>. Counters are organized by   <a href="vim.PerformanceManager.CounterInfo.md#groupInfo">groups</a> of finite system   resources, such as <a href="memory_counters.md">memory</a>, <a   href="cpu_counters.md">CPU</a>, <a href="disk_counters.md">disk</a>, and   so on. The links in this list contain documentation for performance   counters, by <a href="vim.PerformanceManager.CounterInfo.md#groupInfo">group</a>. Each   page contains a table that includes data extracted from instances of the   <a href="vim.PerformanceManager.CounterInfo.md">PerfCounterInfo</a> data object, including the counter   name, its Label, Unit, StatsType, RollupType, and Level: <ul>    <li> <a href="cluster_services_counters.md">Cluster Services</li>   <li> <a href="cpu_counters.md">CPU</a></li>   <li> <a href="hbr_counters.md">Host-Based Replication</a></li>   <li> <a href="mgmt_agent_counters.md">Management Agent</a></li>   <li> <a href="memory_counters.md">Memory</a></li>   <li> <a href="network_counters.md">Network</a></li>   <li> <a href="power_counters.md">Power</a></li>   <li> <a href="resource_scheduler_counters.md">Resource Scheduler</a></li>   <li> Storage Capacity:<ul>      <li> <a href="disk_storutil_counters.md">Datastore / Virtual           Machine</a></li>      </ul></li>   <li> Storage I/O:<ul>      <li> <a href="datastore_counters.md">Datastore</a></li>      <li> <a href="disk_counters.md">Disk</a></li>      <li> <a href="virtual_disk_counters.md">Virtual Disk</a></li>      <li> <a href="storage_adapter_counters.md">Storage Adapter</a></li>      <li> <a href="storage_path_counters.md">Storage Path</a></li>      </ul></li>   <li><a href="system_counters.md">System</a></li>   <li><a href="vcres_counters.md">vCenter Resource</a></li>   <li><a href="vmop_counters.md">Virtual Machine Operations</a></li>   </ul>    <p> Other performance-counter groups, in addition to those listed here,   exist on the system. However, only the counter groups listed are considered   of possible interest to third-party developers.    <p> <b>Obtaining Metadata and Metrics</b><br/> This interface provides these   query operations: <ul>    <li> <a href="vim.PerformanceManager.md#queryProviderSummary">QueryPerfProviderSummary</a>, for obtaining metatdata about <a href="vim.PerformanceManager.ProviderSummary.md">performance providers</a></li>    <li> <a href="vim.PerformanceManager.md#queryCounter">QueryPerfCounter</a> and <a href="vim.PerformanceManager.md#queryCounterByLevel">QueryPerfCounterByLevel</a> for obtaining        metadata about supported counters. </li>    <li> <a href="vim.PerformanceManager.md#queryStats">QueryPerf</a>, <a href="vim.PerformanceManager.md#queryAvailableMetric">QueryAvailablePerfMetric</a>, and <a href="vim.PerformanceManager.md#queryCompositeStats">QueryPerfComposite</a> for obtaining statistics for one or more        entities: <ul>       <li> Use <a href="vim.PerformanceManager.md#queryStats">QueryPerf</a> to obtain metrics for multiple entities in a           single call&#46;</li>       <li> Use <a href="vim.PerformanceManager.md#queryCompositeStats">QueryPerfComposite</a> to obtain statistics for a single           entity with its descendent objects&#151;statistics for a <a href="vim.HostSystem.md">host</a> and all its <a href="vim.VirtualMachine.md">virtual           machines</a>, for example. </li>       </ul> </li>    </ul>    <p> <b>Product and Version Specifics</b><br/> Some differences between ESX   and vCenter Server implementations of this interface include: <ul>    <li> For ESX systems, this interface provides access to real-time data, and        to real-time data that has been rolled up into "PastDay" statistics (if        applicable for the specific counter). </li>    <li> For vCenter Server systems, this interface provides access to real-time        and historical data. vCenter Server collects statistics on a regular        basis from all ESX systems that it manages, and aggregates the results        based on the level settings for the server. </li>    <li> Default sampling interval is product- and version-specific: <ul>       <li> ESX 3&#46;x (and subsequent) systems: 20 second interval</li>       <li> ESX 2&#46;x systems: 60 second interval</li>       </ul> </li>    <li> VirtualCenter Server 2&#46;5 (and subsequent vCenter Server) systems        initially collect statistics data 10 minutes after system startup, and        then hourly thereafter&#46;</li>    </ul>    <p> See the Programming Guide for more information about using <a href="vim.PerformanceManager.md">PerformanceManager</a>&#46;

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='description'>description</a> | [vim.PerformanceDescription](vim.PerformanceDescription.md "vim.PerformanceDescription") | None | System.View | The static description strings. |
| <a href='historicalInterval'>historicalInterval</a> | [vim.HistoricalInterval](vim.HistoricalInterval.md "vim.HistoricalInterval") | true | System.View | A list of <a href="vim.HistoricalInterval.md">intervals</a> configured on the   system. |
| <a href='perfCounter'>perfCounter</a> | [vim.PerformanceManager.CounterInfo](vim.PerformanceManager.CounterInfo.md "vim.PerformanceManager.CounterInfo") | true | System.View | A list of all supported performance counters in the system. |


QueryPerfProviderSummary([entity](#vim.ExtensibleManagedObject "vim.ExtensibleManagedObject"))
----------------------------------------------------------------------------------------------

| service name | QueryPerfProviderSummary |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




QueryAvailablePerfMetric([entity](#vim.ExtensibleManagedObject "vim.ExtensibleManagedObject"), [beginTime](#datetime "datetime"), [endTime](#datetime "datetime"))
------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | QueryAvailablePerfMetric |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the set of arguments passed to the function is   not specified correctly. |




QueryPerfCounter()
------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | QueryPerfCounter |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the set of arguments passed to the function is   not specified correctly. |




QueryPerfCounterByLevel()
-------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | QueryPerfCounterByLevel |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if an invalid level is specified. |




QueryPerf([querySpec](vim.PerformanceManager.QuerySpec.md "vim.PerformanceManager.QuerySpec"))
----------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | QueryPerf |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the set of arguments passed to the function is   not specified correctly. |




QueryPerfComposite([querySpec](vim.PerformanceManager.QuerySpec.md "vim.PerformanceManager.QuerySpec"))
-------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | QueryPerfComposite |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the set of arguments passed to the function is   not specified correctly. |




CreatePerfInterval([intervalId](vim.HistoricalInterval.md "vim.HistoricalInterval"))
------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
### Deprecated
As of API 2.5, use <a href="vim.PerformanceManager.md#updateHistoricalInterval">UpdatePerfInterval</a>. The   default historical intervals can be modified, but they cannot be created.

| service name | CreatePerfInterval |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Performance.ModifyIntervals |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the set of arguments passed to the function is   not specified correctly. |




RemovePerfInterval()
--------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
### Deprecated
As of API 2.5, use <a href="vim.PerformanceManager.md#updateHistoricalInterval">UpdatePerfInterval</a>.   Historical intervals cannot be removed.

| service name | RemovePerfInterval |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Performance.ModifyIntervals |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the set of arguments passed to the function is   not specified correctly. |




UpdatePerfInterval([interval](vim.HistoricalInterval.md "vim.HistoricalInterval"))
----------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | UpdatePerfInterval |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Performance.ModifyIntervals |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the set of arguments passed to the function is   not specified correctly or if the update does not conform to the rules   mentioned above. |




UpdateCounterLevelMapping([counterLevelMap](vim.PerformanceManager.CounterLevelMapping.md "vim.PerformanceManager.CounterLevelMapping"))
----------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | UpdateCounterLevelMapping |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#None) |
| privilege    | Performance.ModifyIntervals |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If the passed in counterId is invalid or if both the aggregateLevel and   perDeviceLevel are unset or if the aggregateLevel field is not between   1-4 (valid values). |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | If called directly on a host. |




ResetCounterLevelMapping()
--------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | ResetCounterLevelMapping |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#None) |
| privilege    | Performance.ModifyIntervals |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If the passed in counterId is invalid. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | If called directly on a host. |




