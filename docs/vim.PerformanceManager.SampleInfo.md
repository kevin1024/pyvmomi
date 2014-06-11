vim.PerformanceManager.SampleInfo
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes information contained in a sample   collection, its timestamp, and sampling interval.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| timestamp | datetime | None | None | The time at which the sample was collected. |
| interval | int | None | None | The interval in seconds for which performance statistics were   collected. This can be the refreshRate of the managed object for which   this statistics was collected or one of the intervals for historical   statistics configured in the system. See <a href="vim.PerformanceManager.md#updateHistoricalInterval">UpdatePerfInterval</a> for more information about the intervals   configured in the system. |


