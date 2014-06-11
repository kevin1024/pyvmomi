vim.storageDrs.SpaceLoadBalanceConfig
=====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Storage DRS configuration for space load balancing.   <p>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| spaceUtilizationThreshold | int | true | None | Storage DRS makes storage migration recommendations if   space utilization on one (or more) of the datastores is higher than   the specified threshold.   <p>   The valid values are in the range of 50 (i.e., 50%) to 100 (i.e., 100%).   If not specified, the default value is 80%. |
| minSpaceUtilizationDifference | int | true | None | Storage DRS considers making storage migration recommendations if   the difference in space utilization between the source and destination datastores   is higher than the specified threshold.   <p>   The valid values are in the range of 1 (i.e., 1%) to 50 (i.e., 50%).   If not specified, the default value is 5%. |


