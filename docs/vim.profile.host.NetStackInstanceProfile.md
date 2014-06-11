vim.profile.host.NetStackInstanceProfile
========================================
inherits from [vim.profile.ApplyProfile](docs/vim.profile.ApplyProfile.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


The <a href="vim.profile.host.NetStackInstanceProfile.md">NetStackInstanceProfile</a> data object represents a subprofile   for a netStackInstance.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Linkable identifier. |
| dnsConfig | [vim.profile.host.NetworkProfile.DnsConfigProfile](vim.profile.host.NetworkProfile.DnsConfigProfile.md "vim.profile.host.NetworkProfile.DnsConfigProfile") | None | None | DnsConfigProfile for this instance of the stack. |
| ipRouteConfig | [vim.profile.host.IpRouteProfile](vim.profile.host.IpRouteProfile.md "vim.profile.host.IpRouteProfile") | None | None | IpRouteProfile for this instance of the stack. |


