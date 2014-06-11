vim.cluster.EnterMaintenanceResult
==================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


EnterMaintenanceResult is the base class of the result returned to the    <a href="vim.ClusterComputeResource.md#enterMaintenanceMode">ClusterEnterMaintenanceMode</a> method.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| recommendations | [vim.cluster.Recommendation](vim.cluster.Recommendation.md "vim.cluster.Recommendation") | true | None | The list of recommendations for hosts that Virtual Center will  be able to evacuate. Each recommendation consists of a host  maintenance action <a href="vim.cluster.Action.md">ClusterAction</a> for a host, along  with zero or more vmotions for evacuation. Application of the  recommendations is not supported currently. The client will have  to put the hosts into maintenance mode by calling the separate  method <a href="vim.HostSystem.md#enterMaintenanceMode">EnterMaintenanceMode_Task</a>. |
| fault | [vim.cluster.DrsFaults](vim.cluster.DrsFaults.md "vim.cluster.DrsFaults") | true | None | The faults that explain why the Virtual Center cannot evacuate  some hosts. |


