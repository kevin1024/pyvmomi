vim.cluster.FailoverLevelAdmissionControlInfo
=============================================
inherits from [vim.cluster.DasAdmissionControlInfo](docs/vim.cluster.DasAdmissionControlInfo.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The current admission control related information if the cluster was configured  with a FailoverLevelAdmissionControlPolicy.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| currentFailoverLevel | int | None | None | Current failover level. This is the number of physical host failures that can   be tolerated without impacting the ability to satisfy the minimums for all   running virtual machines. This represents the current value, as opposed to   desired value configured by the user. |


