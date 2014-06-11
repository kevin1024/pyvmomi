vim.host.SystemSwapConfiguration.DisabledOption
===============================================
inherits from [vim.host.SystemSwapConfiguration.SystemSwapOption](docs/vim.host.SystemSwapConfiguration.SystemSwapOption.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


Indicates that the system swap on the host is currently disabled.   This value is used with the  <a href="vim.HostSystem.md#updateSystemSwapConfiguration">UpdateSystemSwapConfiguration</a> managed method to  disable system swap. Presence of this value in <a href="vim.host.SystemSwapConfiguration.md#option">option</a> excludes appearance of any other  options. Specifying additional options will result in a <a href="vmodl.fault.InvalidArgument.md">InvalidArgument</a> fault being thrown from the <a href="vim.HostSystem.md#updateSystemSwapConfiguration">UpdateSystemSwapConfiguration</a> method.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


