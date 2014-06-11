vim.PerformanceManager.CounterLevelMapping
==========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


<a href="vim.PerformanceManager.CounterLevelMapping.md">PerformanceManagerCounterLevelMapping</a> class captures the counter   and level mapping. Any counter has two aspects: aggregate value or the   per-device value. For example, cpu.usage.average on a host is an   aggregate counter and cpu.usage.average on pcpus in a host is a   per-device counters. There is a need to be able to specify different   levels for the two versions. Currently, all per-device stats are   collected at level greater than or equal to 3.    <p> In order to be able to configure the level of collections for   aggregate and per-device counters we have two optional level fields.   <a href="vim.PerformanceManager.CounterLevelMapping.md">PerformanceManagerCounterLevelMapping</a> is used to update the   levels for a counter.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| counterId | int | None | None | The counter Id |
| aggregateLevel | int | true | None | Level for the aggregate counter. If not set then the value is not   changed when updateCounterLevelMapping is called. |
| perDeviceLevel | int | true | None | Level for the per device counter. If not set then the value is not   changed when updateCounterLevelMapping is called. |


