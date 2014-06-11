vim.vm.ToolsConfigInfo.ToolsLastInstallInfo
===========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Describes status of last tools upgrade attempt

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| counter | int | None | None | Number of attempts that have been made to upgrade the version of tools  installed on this virtual machine. |
| fault | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | Error that happened, if any, during last attempt to upgrade tools. |


