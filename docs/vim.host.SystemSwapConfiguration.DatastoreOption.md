vim.host.SystemSwapConfiguration.DatastoreOption
================================================
inherits from [vim.host.SystemSwapConfiguration.SystemSwapOption](docs/vim.host.SystemSwapConfiguration.SystemSwapOption.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


Use option to indicate that a user specified datastore may be used for  system swap.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| datastore | string | None | None | The datastore to be used with this swap option.   This value should be always set when the encapsulating option is used,  otherwise a call to <a href="vim.HostSystem.md#updateSystemSwapConfiguration">UpdateSystemSwapConfiguration</a> will  result in a <a href="vmodl.fault.InvalidArgument.md">InvalidArgument</a> fault. |


