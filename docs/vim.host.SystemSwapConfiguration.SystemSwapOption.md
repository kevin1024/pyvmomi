vim.host.SystemSwapConfiguration.SystemSwapOption
=================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


Base class for all system swap options.   This class is not supposed to be used directly.<br/>  These values are to be used in a <a href="vim.host.SystemSwapConfiguration.md#option">SystemSwapConfiguration.option</a>  array.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | int | None | None | Specifies the order the options are prefered among each other.   The lower the value the more important. |


