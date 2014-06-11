vim.vm.MetadataManager.VmMetadataOwner
======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


VmMetadataOwner defines the namespace for an owner

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | A string representing the owner. Valid values come  from Owner for vSAN datastores.  Otherwise, the  owner field is interpreted by the implementation based on  the datastore type. |


