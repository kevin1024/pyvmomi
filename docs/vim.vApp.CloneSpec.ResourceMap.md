vim.vApp.CloneSpec.ResourceMap
==============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Maps source child entities to destination resource pools   and resource settings. If a mapping is not specified,   a child is copied as a direct child of the parent.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| source | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | None | None | Source entity |
| parent | [vim.ResourcePool](vim.ResourcePool.md "vim.ResourcePool") | true | Resource.AssignVAppToPool | Resource pool to use for the cloned entity of source. This must specify a    resource pool that is not part of the vApp. If this is specified, a linked   child (as opposed to a direct child) is created for the vApp. |
| resourceSpec | [vim.ResourceConfigSpec](vim.ResourceConfigSpec.md "vim.ResourceConfigSpec") | true | None | An optional resource configuration for the cloned entity of the source. If    not specified, the same resource configuration as the source is used. |
| location | [vim.Datastore](vim.Datastore.md "vim.Datastore") | true | Datastore.AllocateSpace | A client can optionally specify a datastore in the resource map to   override the default datastore location set in <a href="vim.vApp.CloneSpec.ResourceMap.md#location">location</a> field. This   enables cloning to different compute resources that do not have shared   datastores. |


