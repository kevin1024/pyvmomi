vim.storageDrs.IoLoadBalanceConfig
==================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Storage DRS configuration for I/O load balancing.   <p>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ioLatencyThreshold | int | true | None | Storage DRS makes storage migration recommendations if   I/O latency on one (or more) of the datastores is higher than   the specified threshold.   <p>   Unit: millisecond.   The valid values are in the range of 5 to 100. If not specified,   the default value is 15. |
| ioLoadImbalanceThreshold | int | true | None | Storage DRS makes storage migration recommendations if   I/O load imbalance level is higher than the specified threshold.   <p>   Unit: a number.   The valid values are in the range of 1 to 100. If not specified,   the default value is 5. |


