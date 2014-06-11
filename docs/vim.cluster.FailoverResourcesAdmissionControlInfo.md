vim.cluster.FailoverResourcesAdmissionControlInfo
=================================================
inherits from [vim.cluster.DasAdmissionControlInfo](docs/vim.cluster.DasAdmissionControlInfo.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The current admission control related information if the cluster was configured  with a FailoverResourcesAdmissionControlPolicy.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| currentCpuFailoverResourcesPercent | int | None | None | The percentage of cpu resources in the cluster available for failover. |
| currentMemoryFailoverResourcesPercent | int | None | None | The percentage of memory resources in the cluster available for failover. |


