vim.PerformanceManager.QuerySpec
================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object specifies the query parameters, including the managed   object reference to the target entity for statistics retrieval. <ul>    <li> If the optional <a href="vim.PerformanceManager.QuerySpec.md#intervalId">intervalId</a> is omitted, the metrics are        returned in their originally sampled interval. <ul>       <li> When an <a href="vim.PerformanceManager.QuerySpec.md#intervalId">intervalId</a> is specified, the server tries to           summarize the information for the specified <a href="vim.PerformanceManager.QuerySpec.md#intervalId">intervalId</a>.           However, if that interval does not exist or has no data, the           server summarizes the information using the best interval           available. </li>       </ul> </li>    <li> If the range between <a href="vim.PerformanceManager.QuerySpec.md#startTime">startTime</a> and <a href="vim.PerformanceManager.QuerySpec.md#endTime">endTime</a> crosses        multiple sample interval periods, the result contains data from the        longest interval in the period. </li>    </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entity | vim.ExtensibleManagedObject | None | None | The managed object whose performance statistics are being queried. |
| startTime | datetime | true | None | The server time from which to obtain counters. If not specified,   defaults to the first available counter. When a startTime is   specified, the returned samples do not include the sample at   startTime. |
| endTime | datetime | true | None | The time up to which statistics are retrieved. Corresponds to server   time. When endTime is omitted, the returned result includes up to the   most recent metric value. When an endTime is specified, the returned   samples include the sample at endTime. |
| maxSample | int | true | None | Limits the number of samples returned. Defaults to the most recent   sample (or samples), unless a time range is specified. Use this   property only in conjunction with the <a href="vim.PerformanceManager.QuerySpec.md#intervalId">intervalId</a> to obtain   real-time statistics (set the <a href="vim.PerformanceManager.QuerySpec.md#intervalId">intervalId</a> to the <a href="vim.PerformanceManager.ProviderSummary.md#refreshRate">refreshRate</a>. This property is   ignored for historical statistics, and is not valid for the <a href="vim.PerformanceManager.md#queryCompositeStats">QueryPerfComposite</a> operation. |
| metricId | [vim.PerformanceManager.MetricId](vim.PerformanceManager.MetricId.md "vim.PerformanceManager.MetricId") | true | None | The performance metrics to be retrieved. This property is required for   the <a href="vim.PerformanceManager.md#queryCompositeStats">QueryPerfComposite</a> operation. |
| intervalId | int | true | None | The interval (<a href="vim.HistoricalInterval.md#samplingPeriod">samplingPeriod</a>), in seconds,   for the performance statistics&#46; For aggregated information, use   one of the historical intervals for this property. See <a href="vim.HistoricalInterval.md">PerfInterval</a> for more information. <ul>    <li> To obtain the greatest detail, use the provider&#146;s <a href="vim.PerformanceManager.ProviderSummary.md#refreshRate">refreshRate</a> for this        property.    </ul> |
| format | string | true | None | The format to be used while returning the statistics&#46;<br>See <a href="vim.PerformanceManager.Format.md">PerfFormat</a><br> |


