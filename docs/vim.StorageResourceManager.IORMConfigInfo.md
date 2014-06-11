vim.StorageResourceManager.IORMConfigInfo
=========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Configuration of storage I/O resource management.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| enabled | bool | None | None | Flag indicating whether or not the service is enabled. |
| congestionThresholdMode | string | None | None | Mode of congestion threshold specification  For more information, see  <a href="vim.StorageResourceManager.CongestionThresholdMode.md">StorageIORMThresholdMode</a> |
| congestionThreshold | int | None | None | The latency beyond which the storage array is considered congested.   <p>   If storage I/O resource management is enabled on a datastore,   the algorithm tries to maintain the latency to be below or   close to this value. The unit is millisecond. The range of   this value is between 5 to 100 milliseconds. |
| percentOfPeakThroughput | int | true | None | The percentage of peak throughput to be used for setting congestion threshold  of a datastore. Valid values are between 50 to 100. Default value is 90%  <p>  For more information, see   <a href="vim.StorageResourceManager.IORMConfigInfo.md#congestionThreshold">congestionThreshold</a> |
| statsCollectionEnabled | bool | None | None | Flag indicating whether service is running in stats collection mode. |
| statsAggregationDisabled | bool | true | None | Flag indicating whether stats aggregation is disabled. |


