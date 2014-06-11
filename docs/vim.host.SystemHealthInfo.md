vim.host.SystemHealthInfo
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This data object provides information about the health of the phyical   system. The data is retrieved from numeric sensor probes.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| numericSensorInfo | [vim.host.NumericSensorInfo](vim.host.NumericSensorInfo.md "vim.host.NumericSensorInfo") | true | None | Health information provided by the power probes. |


