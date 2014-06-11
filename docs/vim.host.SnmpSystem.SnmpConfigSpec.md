vim.host.SnmpSystem.SnmpConfigSpec
==================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| enabled | bool | true | None |  |
| port | int | true | None |  |
| readOnlyCommunities | string | true | None |  |
| trapTargets | [vim.host.SnmpSystem.SnmpConfigSpec.Destination](vim.host.SnmpSystem.SnmpConfigSpec.Destination.md "vim.host.SnmpSystem.SnmpConfigSpec.Destination") | true | None |  |
| option | [vim.KeyValue](vim.KeyValue.md "vim.KeyValue") | true | None |  |


