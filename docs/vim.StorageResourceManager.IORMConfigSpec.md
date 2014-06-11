vim.StorageResourceManager.IORMConfigSpec
=========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Configuration settings used for creating or reconfiguring   storage I/O resource management.   <p>   All fields are defined as optional. If a field is unset,   the property is not changed.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| enabled | bool | true | None | Flag indicating whether or not the service is enabled. |
| congestionThresholdMode | string | true | None | Mode of congestion threshold specification  For more information, see  <a href="vim.StorageResourceManager.CongestionThresholdMode.md">StorageIORMThresholdMode</a> |
| congestionThreshold | int | true | None | The latency beyond which the storage array is considered congested.   <p>   For more information, see   <a href="vim.StorageResourceManager.IORMConfigInfo.md#congestionThreshold">congestionThreshold</a> |
| percentOfPeakThroughput | int | true | None | The percentage of peak throughput to be used for setting threshold latency  of a datastore. Valid values are between 50 to 100.  <p>  For more information, see   <a href="vim.StorageResourceManager.IORMConfigInfo.md#congestionThreshold">congestionThreshold</a> |
| statsCollectionEnabled | bool | true | None | Flag indicating whether the service is enabled in stats collection mode. |
| statsAggregationDisabled | bool | true | None | Flag indicating whether stats aggregation is disabled. |


