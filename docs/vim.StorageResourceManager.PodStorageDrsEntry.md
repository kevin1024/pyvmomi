vim.StorageResourceManager.PodStorageDrsEntry
=============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


An entry containing storage DRS configuration, runtime   results, and history for a pod <a href="vim.StoragePod.md">StoragePod</a>.   <p>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| storageDrsConfig | [vim.storageDrs.ConfigInfo](vim.storageDrs.ConfigInfo.md "vim.storageDrs.ConfigInfo") | None | None | Storage DRS configuration. |
| recommendation | [vim.cluster.Recommendation](vim.cluster.Recommendation.md "vim.cluster.Recommendation") | true | None | List of recommended actions for the Storage Pod. It is   possible that the current set of recommendations may be empty,   either due to not having any running dynamic recommendation   generation module, or since there may be no recommended actions   at this time. |
| drsFault | [vim.cluster.DrsFaults](vim.cluster.DrsFaults.md "vim.cluster.DrsFaults") | true | None | A collection of the DRS faults generated in the last Storage DRS invocation.  Each element of the collection is the set of faults generated in one  recommendation. |
| actionHistory | [vim.cluster.ActionHistory](vim.cluster.ActionHistory.md "vim.cluster.ActionHistory") | true | None | The set of actions that have been performed recently. |


