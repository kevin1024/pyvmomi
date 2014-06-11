vim.storageDrs.StoragePlacementResult
=====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Both <a href="vim.StorageResourceManager.md#recommendDatastores">RecommendDatastores</a> and    <a href="vim.Datastore.md#enterMaintenanceMode">DatastoreEnterMaintenanceMode</a> methods may invoke Storage DRS    for recommendations on placing or evacuating virtual disks.    StoragePlacementResult is the class of the result returned by    the methods.    <p>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| recommendations | [vim.cluster.Recommendation](vim.cluster.Recommendation.md "vim.cluster.Recommendation") | true | None | The list of recommendations that the client needs to approve manually. |
| drsFault | [vim.cluster.DrsFaults](vim.cluster.DrsFaults.md "vim.cluster.DrsFaults") | true | None | Information about any fault in case Storage DRS failed to make a recommendation. |
| task | [vim.Task](vim.Task.md "vim.Task") | true | None | The ID of the task, which monitors the storage placement or datastore entering   maintennace mode operation. |


