vim.SharesOption
================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Specification of shares.   <p>   Object of this class specifies value ranges for object of   instance <a href="vim.SharesInfo.md">SharesInfo</a>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| sharesOption | [vim.option.IntOption](vim.option.IntOption.md "vim.option.IntOption") | None | None | Value range which can be used for share definition  in <a href="vim.SharesInfo.md#shares">shares</a> |
| defaultLevel | [vim.SharesInfo.Level](vim.SharesInfo.Level.md "vim.SharesInfo.Level") | None | None | Default value for <a href="vim.SharesInfo.md#level">level</a> |


