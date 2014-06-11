vim.storageDrs.ConfigSpec
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


The <a href="vim.storageDrs.ConfigSpec.md">StorageDrsConfigSpec</a> data object provides a set of update   specifications for storage DRS configuration. To support   incremental changes, these properties are all optional.   <p>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| podConfigSpec | [vim.storageDrs.PodConfigSpec](vim.storageDrs.PodConfigSpec.md "vim.storageDrs.PodConfigSpec") | true | None | Changes to the configuration of the storage DRS service. |
| vmConfigSpec | [vim.storageDrs.VmConfigSpec](vim.storageDrs.VmConfigSpec.md "vim.storageDrs.VmConfigSpec") | true | None | Changes to the per-virtual-machine storage DRS settings. |


