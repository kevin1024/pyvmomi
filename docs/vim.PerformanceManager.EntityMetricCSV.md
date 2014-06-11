vim.PerformanceManager.EntityMetricCSV
======================================
inherits from [vim.PerformanceManager.EntityMetricBase](docs/vim.PerformanceManager.EntityMetricBase.md)


This data object type stores metric values for a specific entity in CSV   format.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| sampleInfoCSV | string | None | None | The <a href="vim.PerformanceManager.SampleInfo.md">PerfSampleInfo</a> encoded in the following CSV   format: [interval1], [date1], [interval2], [date2], and so on. |
| value | [vim.PerformanceManager.MetricSeriesCSV](vim.PerformanceManager.MetricSeriesCSV.md "vim.PerformanceManager.MetricSeriesCSV") | true | None | Metric values corresponding to the samples collected in this list. |


