vim.StorageResourceManager.IOAllocationOption
=============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


The IOAllocationOption specifies value ranges that can be used  to initialize IOAllocationInfo object.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| limitOption | [vim.option.LongOption](vim.option.LongOption.md "vim.option.LongOption") | None | None | limitOptions defines a range of values allowed to be used for  storage IO limit <a href="vim.StorageResourceManager.IOAllocationInfo.md#limit">limit</a>. |
| sharesOption | [vim.SharesOption](vim.SharesOption.md "vim.SharesOption") | None | None | sharesOption defines a range of values allowed to be used to  specify allocated io shares <a href="vim.StorageResourceManager.IOAllocationInfo.md#shares">shares</a>. |


