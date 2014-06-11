vim.StorageResourceManager.StoragePerformanceSummary
====================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


Summary statistics for datastore performance   The statistics are reported in aggregated quantiles over a time period

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| interval | int | None | None | Time period over which statistics are aggregated  The reported time unit is in seconds |
| percentile | int | None | None | Metric percentile specification. A percentile is a value  between 1 and 100. The metric value reported in the  aggregated statistics corresponds with the percentile values  in this field. For example, if the value of percentile[0] is  P, and the value of the datastoreReadLatency[0] is L, then  P% of all the read IOs performed during observation interval  is less than L milliseconds. |
| datastoreReadLatency | double | None | None | Aggregated datastore latency in milliseconds for read operations |
| datastoreWriteLatency | double | None | None | Aggregated datastore latency in milliseconds for write operations |
| datastoreVmLatency | double | None | None | Aggregated datastore latency as observed by Vms using the datastore  The reported latency is in milliseconds. |
| datastoreReadIops | double | None | None | Aggregated datastore Read IO rate (Reads/second) |
| datastoreWriteIops | double | None | None | Aggregated datastore Write IO rate (Writes/second) |
| siocActivityDuration | int | None | None | Cumulative SIOC activity to satisfy SIOC latency threshold  setting.  This metric indicates the total time that SIOC is  actively throttling IO requests. The SIOC throttling  activity occurs whenever the datastore latency exceeds the  SIOC latency threshold. If SIOC is not enabled on the  datastore, the metric indicates the total time that SIOC  would have been active. The unit of reporting is in  milliseconds. |


