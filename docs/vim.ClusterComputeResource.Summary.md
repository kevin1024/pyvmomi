vim.ClusterComputeResource.Summary
==================================
inherits from [vim.ComputeResource.Summary](docs/vim.ComputeResource.Summary.md)


The <a href="vim.ClusterComputeResource.Summary.md">ClusterComputeResourceSummary</a> data object   encapsulates runtime properties of a <a href="vim.ClusterComputeResource.md">ClusterComputeResource</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| currentFailoverLevel | int | None | None | Current failover level. This is the number of physical host failures that can   be tolerated without impacting the ability to satisfy the minimums for all   running virtual machines. This represents the current value, as opposed to   desired value configured by the user. |
| admissionControlInfo | [vim.cluster.DasAdmissionControlInfo](vim.cluster.DasAdmissionControlInfo.md "vim.cluster.DasAdmissionControlInfo") | true | None | Information about the current amount of resources available for a vSphere HA  cluster. The actual type of admissionControlInfo will depend on what kind of  <a href="vim.cluster.DasAdmissionControlPolicy.md">ClusterDasAdmissionControlPolicy</a> was used to configure the cluster. |
| numVmotions | int | None | None | Total number of migrations with VMotion that have been done internal to this   cluster. |
| targetBalance | int | true | None | The target balance, in terms of standard deviation, for a DRS cluster.   Units are thousandths. For example, 12 represents 0.012. |
| currentBalance | int | true | None | The current balance, in terms of standard deviation, for a DRS cluster.   Units are thousandths. For example, 12 represents 0.012. |
| currentEVCModeKey | string | true | None | The Enhanced VMotion Compatibility mode that is currently in effect   for all hosts in this cluster; unset if no EVC mode is active.<br>See <a href="vim.Capability.md#supportedEVCMode">supportedEVCMode</a><br> |
| dasData | [vim.cluster.DasData](vim.cluster.DasData.md "vim.cluster.DasData") | true | None | Data pertaining to DAS. |


