vim.storageDrs.ApplyRecommendationResult
========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Both <a href="vim.StorageResourceManager.md#recommendDatastores">RecommendDatastores</a> and    <a href="vim.Datastore.md#enterMaintenanceMode">DatastoreEnterMaintenanceMode</a> methods may invoke Storage DRS    for recommendations on placing or evacuating virtual disks.    All initial placement recommendations, and some enterMaintenanceMode    recommendations need to be approved by the user. Recommendations that    are approved will be applied using the     <a href="vim.StorageResourceManager.md#applyRecommendation">ApplyStorageDrsRecommendation_Task</a>     method.     This class encapsulates the result of applying a subset of the    recommendations.    <p>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vm | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | true | None | The result applying the recommendation, if it was successful.  This is the equivalent of the <a href="vim.TaskInfo.md#result">result</a> key for the  task launched when the recommendation was applied. |


