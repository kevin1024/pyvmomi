vim.profile.host.IpRouteProfile
===============================
inherits from [vim.profile.ApplyProfile](docs/vim.profile.ApplyProfile.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.host.IpRouteProfile.md">IpRouteProfile</a> data object represents the host IP route configuration.  If a profile plug-in defines policies or subprofiles, use the  <a href="vim.profile.ApplyProfile.md#policy">policy</a> or <a href="vim.profile.ApplyProfile.md#property">property</a>  list to access the additional configuration data.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| staticRoute | [vim.profile.host.StaticRouteProfile](vim.profile.host.StaticRouteProfile.md "vim.profile.host.StaticRouteProfile") | true | None | List of static routes to be configured. |


