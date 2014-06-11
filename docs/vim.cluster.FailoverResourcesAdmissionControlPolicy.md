vim.cluster.FailoverResourcesAdmissionControlPolicy
===================================================
inherits from [vim.cluster.DasAdmissionControlPolicy](docs/vim.cluster.DasAdmissionControlPolicy.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.cluster.FailoverResourcesAdmissionControlPolicy.md">ClusterFailoverResourcesAdmissionControlPolicy</a>  reserves a specified percentage of aggregate cluster resources for failover.  With the resources failover policy in place, vSphere HA uses the following  calculations to control virtual machine migration in the cluster.  <ol>  <li>Calculate the total resource requirements for all powered-on      virtual machines in the cluster.  <li>Calculate the total host resources available for virtual machines.  <li>Calculate the Current CPU failover capacity and current memory failover      capacity for the cluster.  <li>Compare the current CPU failover capacity and current memory failover      capacity with the configured resource percentages      (<a href="vim.cluster.FailoverResourcesAdmissionControlPolicy.md#cpuFailoverResourcesPercent">cpuFailoverResourcesPercent</a>      and      <a href="vim.cluster.FailoverResourcesAdmissionControlPolicy.md#memoryFailoverResourcesPercent">memoryFailoverResourcesPercent</a>).      If either current capacity is less than the corresponding configured      capacity, HA does not allow the operation.  </ol>  <p>  HA uses the actual reservations of the virtual machines. If a virtual machine  does not have reservations, meaning that the reservation is 0, a default  of 0MB memory and 256MHz CPU is applied. This is controlled by the same  HA advanced options used for the failover level policy  (<a href="vim.cluster.FailoverLevelAdmissionControlPolicy.md">ClusterFailoverLevelAdmissionControlPolicy</a>).

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| cpuFailoverResourcesPercent | int | None | None | Percentage of CPU resources in the cluster to reserve for failover.  You can specify up to 100% of CPU resources for failover. |
| memoryFailoverResourcesPercent | int | None | None | Percentage of memory resources in the cluster to reserve for failover.  You can specify up to 100% of memory resources for failover. |


