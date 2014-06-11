vim.cluster.FailoverHostAdmissionControlPolicy
==============================================
inherits from [vim.cluster.DasAdmissionControlPolicy](docs/vim.cluster.DasAdmissionControlPolicy.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.cluster.FailoverHostAdmissionControlPolicy.md">ClusterFailoverHostAdmissionControlPolicy</a> dedicates  one or more hosts for use during failover.  When a host fails with this policy in place, vSphere HA attempts  to restart its virtual machines on a dedicated failover host.  If this is not possible, for example the failover host itself has failed  or it has insufficient resources, HA attempts to restart those virtual  machines on another host in the cluster.  <p>  To support the availabilty of a failover host,  the vCenter Server will prevent users from powering on virtual machines  on that host, or from using vMotion to migrate virtual machines to the host.  Also, DRS does not use the failover host for load balancing.  <p>  To obtain the status of a failover host, use the  <a href="vim.cluster.FailoverHostAdmissionControlInfo.md#hostStatus">hostStatus</a>  property  (<a href="vim.ClusterComputeResource.Summary.md">ClusterComputeResourceSummary</a>.<a href="vim.ClusterComputeResource.Summary.md#admissionControlInfo">admissionControlInfo</a>.<a href="vim.cluster.FailoverHostAdmissionControlInfo.md#hostStatus">hostStatus</a>).

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| failoverHosts | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | true | None | List of managed object references to failover hosts. |


