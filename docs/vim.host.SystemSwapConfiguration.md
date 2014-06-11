vim.host.SystemSwapConfiguration
================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


Information and specification for control of the system swap configuration  on the current host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| option | [vim.host.SystemSwapConfiguration.SystemSwapOption](vim.host.SystemSwapConfiguration.SystemSwapOption.md "vim.host.SystemSwapConfiguration.SystemSwapOption") | true | None | The currently enabled options.   When this property contains only one value and this value is <a href="vim.host.SystemSwapConfiguration.DisabledOption.md">HostSystemSwapConfigurationDisabledOption</a>,  this indicates that the system swap is disabled.<br/>  If the <a href="vim.host.SystemSwapConfiguration.DisabledOption.md">HostSystemSwapConfigurationDisabledOption</a> option is  used toghether with some other option in call to <a href="vim.HostSystem.md#updateSystemSwapConfiguration">UpdateSystemSwapConfiguration</a>, a  <a href="vmodl.fault.InvalidArgument.md">InvalidArgument</a> is thrown.<br/>  It is not allowed to have duplicate values in this array. If so a  <a href="vmodl.fault.InvalidArgument.md">InvalidArgument</a> is thrown.<br/> |


