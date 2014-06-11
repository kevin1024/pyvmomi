vim.dvs.DistributedVirtualSwitchManager.DvsProductSpec
======================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


This class is used to specify ProductSpec for the DVS. The two properties are  strictly mutually exclusive. If both properties are set, then  an InvalidArgument fault would be thrown.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| newSwitchProductSpec | [vim.dvs.ProductSpec](vim.dvs.ProductSpec.md "vim.dvs.ProductSpec") | true | None | The ProductSpec for new DVS |
| distributedVirtualSwitch | [vim.DistributedVirtualSwitch](vim.DistributedVirtualSwitch.md "vim.DistributedVirtualSwitch") | true | None | Get ProductSpec from the existing DVS |


