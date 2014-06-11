vim.vApp.CloneSpec.NetworkMappingPair
=====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Maps one network to another as part of the clone process.  <p>  Instances of this class are used in the field <a href="vim.vApp.CloneSpec.md#networkMapping">networkMapping</a>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| source | [vim.Network](vim.Network.md "vim.Network") | None | None | The source network |
| destination | [vim.Network](vim.Network.md "vim.Network") | None | Network.Assign | The destination network |


