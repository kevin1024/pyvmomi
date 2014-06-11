vim.host.NetworkConfig.NetStackSpec
===================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This data type describes Network Stack Spec

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| netStackInstance | [vim.host.NetStackInstance](vim.host.NetStackInstance.md "vim.host.NetStackInstance") | None | None | Network stack instance |
| operation | string | true | None | Operation type, see   <a href="vim.ConfigSpecOperation.md">ConfigSpecOperation</a> for valid values.   Only edit operation is supported currently. |


