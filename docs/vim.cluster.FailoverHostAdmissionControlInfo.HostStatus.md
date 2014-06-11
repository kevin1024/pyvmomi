vim.cluster.FailoverHostAdmissionControlInfo.HostStatus
=======================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Data object containing the status of a failover host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| host | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | None | None | The failover host. |
| status | [vim.ManagedEntity.Status](vim.ManagedEntity.Status.md "vim.ManagedEntity.Status") | None | None | The status of the failover host.    The status is green for a connected host with no vSphere HA errors and   no virtual machines running on it.  The status is yellow for a connected host with no vSphere HA errors and  some virtual machines running on it.  The status red for a disconnected or not responding host, a host that  is in maintenance or standby mode or that has a vSphere HA error on it. |


