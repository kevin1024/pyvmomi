vim.cluster.FailoverHostAdmissionControlInfo
============================================
inherits from [vim.cluster.DasAdmissionControlInfo](docs/vim.cluster.DasAdmissionControlInfo.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The current admission control related information if the cluster was configured  with a FailoverHostAdmissionControlPolicy.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| hostStatus | [vim.cluster.FailoverHostAdmissionControlInfo.HostStatus](vim.cluster.FailoverHostAdmissionControlInfo.HostStatus.md "vim.cluster.FailoverHostAdmissionControlInfo.HostStatus") | true | None | Status of the failover hosts in the cluster. |


