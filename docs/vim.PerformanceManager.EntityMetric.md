vim.PerformanceManager.EntityMetric
===================================
inherits from [vim.PerformanceManager.EntityMetricBase](docs/vim.PerformanceManager.EntityMetricBase.md)


This data object type stores values and metadata for metrics associated   with a specific entity, in 'normal'  format.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| sampleInfo | [vim.PerformanceManager.SampleInfo](vim.PerformanceManager.SampleInfo.md "vim.PerformanceManager.SampleInfo") | true | None | A list of objects containing information (an interval and a timestamp)   about the samples collected. |
| value | [vim.PerformanceManager.MetricSeries](vim.PerformanceManager.MetricSeries.md "vim.PerformanceManager.MetricSeries") | true | None | A list of values that corresponds to the samples collected. |


