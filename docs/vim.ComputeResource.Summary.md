vim.ComputeResource.Summary
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type encapsulates a typical set of ComputeResource information   that is useful for list views and summary pages.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| totalCpu | int | None | None | Aggregated CPU resources of all hosts, in MHz. |
| totalMemory | long | None | None | Aggregated memory resources of all hosts, in bytes. |
| numCpuCores | short | None | None | Number of physical CPU cores. Physical CPU cores are the processors contained   by a CPU package. |
| numCpuThreads | short | None | None | Aggregated number of CPU threads. |
| effectiveCpu | int | None | None | Effective CPU resources (in MHz) available to run virtual machines. This is the   aggregated effective resource level from all running hosts. Hosts that are in   maintenance mode or are unresponsive are not counted. Resources used by the   VMware Service Console are not included in the aggregate. This value represents   the amount of resources available for the root resource pool for running   virtual machines. |
| effectiveMemory | long | None | None | Effective memory resources (in MB) available to run virtual machines.   This is the aggregated effective resource level from all running hosts. Hosts   that are in maintenance mode or are unresponsive are not counted.   Resources used by the VMware Service Console are not included in the aggregate.   This value represents the amount of resources available for the root   resource pool for running virtual machines. |
| numHosts | int | None | None | Total number of hosts. |
| numEffectiveHosts | int | None | None | Total number of effective hosts. |
| overallStatus | [vim.ManagedEntity.Status](vim.ManagedEntity.Status.md "vim.ManagedEntity.Status") | None | None | Overall alarm status.    In releases after vSphere API 5.0, vSphere Servers might not   generate property collector update notifications for this property.   To obtain the latest value of the property, you can use   PropertyCollector methods RetrievePropertiesEx or WaitForUpdatesEx.   If you use the PropertyCollector.WaitForUpdatesEx method, specify   an empty string for the version parameter.    Since this property is on a DataObject, an update returned by WaitForUpdatesEx may   contain values for this property when some other property on the DataObject changes.   If this update is a result of a call to WaitForUpdatesEx with a non-empty   version parameter, the value for this property may not be current. |


