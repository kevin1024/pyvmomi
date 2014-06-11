vim.PerformanceManager.ProviderSummary
======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type contains information about a performance provider,   the type of statistics it generates, and the <a href="vim.PerformanceManager.ProviderSummary.md#refreshRate">refreshRate</a> for   statistics generation. A performance provider is any <a href="vim.ExtensibleManagedObject.md">managed object</a> that generates real-time or   historical statistics (or both&#151;the <a href="vim.PerformanceManager.ProviderSummary.md#currentSupported">currentSupported</a> and   <a href="vim.PerformanceManager.ProviderSummary.md#summarySupported">summarySupported</a> properties are not mutually exclusive).

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entity | vim.ExtensibleManagedObject | None | None | Reference to the performance provider, the <a href="vim.ExtensibleManagedObject.md">managed object</a> that provides real-time or   historical metrics. The managed objects include but are not limited to   <a href="vim.ManagedEntity.md">managed entities</a>, such as <a href="vim.HostSystem.md">host systems</a>, <a href="vim.VirtualMachine.md">virtual machines</a>, and <a href="vim.ResourcePool.md">resource pools</a>. |
| currentSupported | bool | None | None | True if this entity supports real-time (current) statistics; false if   it does not. If this property is true for an entity, a client application   can set the <a href="vim.PerformanceManager.QuerySpec.md#intervalId">intervalId</a> of the   <a href="vim.PerformanceManager.QuerySpec.md">PerfQuerySpec</a> (passed to the   <a href="vim.PerformanceManager.md#queryStats">QueryPerf</a> operation) to the <a href="vim.PerformanceManager.ProviderSummary.md#refreshRate">refreshRate</a> to obtain the maximum information possible for the   entity. |
| summarySupported | bool | None | None | True if this entity supports historical (aggregated) statistics; false   if it does not. When this property is true for an entity, a client   application can set the <a href="vim.PerformanceManager.QuerySpec.md#intervalId">intervalId</a> of <a href="vim.PerformanceManager.md#queryStats">QueryPerf</a> to one of the historical <a href="vim.HistoricalInterval.md">intervals</a> to obtain historical statistics for this   entity. |
| refreshRate | int | true | None | Number of seconds between the generation of each counter. This value   applies only to entities that support real-time (current)   statistics&#46; |


