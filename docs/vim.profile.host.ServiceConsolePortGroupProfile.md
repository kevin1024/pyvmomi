vim.profile.host.ServiceConsolePortGroupProfile
===============================================
inherits from [vim.profile.host.PortGroupProfile](docs/vim.profile.host.PortGroupProfile.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.host.ServiceConsolePortGroupProfile.md">ServiceConsolePortGroupProfile</a> data object represents   the profile for a port group that will be used by the service console.   If a profile plug-in defines policies or subprofiles, use the   <a href="vim.profile.ApplyProfile.md#policy">policy</a> or <a href="vim.profile.ApplyProfile.md#property">property</a>   list to access the additional configuration data.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ipConfig | [vim.profile.host.IpAddressProfile](vim.profile.host.IpAddressProfile.md "vim.profile.host.IpAddressProfile") | None | None | IP address configuration for the service console network. |


