vim.PerformanceManager.CompositeEntityMetric
============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


<a href="vim.PerformanceManager.CompositeEntityMetric.md">PerfCompositeMetric</a> includes an optional   aggregated entity performance statistics and a list of composite entities   performance statistics&#46; The aggregated entity statistics are optional   because some entities, such as folders, do not have their own   statistics&#46;

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entity | [vim.PerformanceManager.EntityMetricBase](vim.PerformanceManager.EntityMetricBase.md "vim.PerformanceManager.EntityMetricBase") | true | None | The aggregated entity performance metrics. If it exists, the <a href="vim.PerformanceManager.SampleInfo.md">PerfSampleInfo</a> list of the aggregate entity is a   complete list of <a href="vim.PerformanceManager.SampleInfo.md">PerfSampleInfo</a> that could   be contained in <a href="vim.PerformanceManager.SampleInfo.md">PerfSampleInfo</a> lists of   child entities. |
| childEntity | [vim.PerformanceManager.EntityMetricBase](vim.PerformanceManager.EntityMetricBase.md "vim.PerformanceManager.EntityMetricBase") | true | None | A list of <a href="vim.PerformanceManager.EntityMetric.md">metrics</a> of   performance providers that comprise the aggregated entity. For   example, Host is an aggregated entity for virtual machines and   virtual machine Folders. ResourcePools are aggregate entities for   virtual machines. Host, Folder, and Cluster are aggregate entities   for hosts in the cluster or folder. |


