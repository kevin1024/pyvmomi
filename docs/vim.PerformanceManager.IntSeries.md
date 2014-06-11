vim.PerformanceManager.IntSeries
================================
inherits from [vim.PerformanceManager.MetricSeries](docs/vim.PerformanceManager.MetricSeries.md)


This data object type describes integer metric values. The size of the   array must match the size of <a href="vim.PerformanceManager.EntityMetric.md#sampleInfo">sampleInfo</a> property in the <a href="vim.PerformanceManager.EntityMetric.md">PerfEntityMetric</a> that contains this series.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| value | long | true | None | An array of 64-bit integer values. The size of the array matches the   size as the <a href="vim.PerformanceManager.SampleInfo.md">PerfSampleInfo</a>, because the values   can only be interpreted in the context of the sample that generated   the value. |


