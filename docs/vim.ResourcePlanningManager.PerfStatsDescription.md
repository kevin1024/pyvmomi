vim.ResourcePlanningManager.PerfStatsDescription
================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Data object to capture all information needed to   describe a sample inventory.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| intervals | [vim.HistoricalInterval](vim.HistoricalInterval.md "vim.HistoricalInterval") | true | None | Historic interval setting.   Default value is the same as the historic  interval settings of the current instance  of running VC. |


