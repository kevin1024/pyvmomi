vim.profile.host.DvsProfile
===========================
inherits from [vim.profile.ApplyProfile](docs/vim.profile.ApplyProfile.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.host.DvsProfile.md">DvsProfile</a> data object represents the distributed virtual switch  to which this host is connected. If a profile plug-in defines policies or subprofiles,  use the <a href="vim.profile.ApplyProfile.md#policy">policy</a> or <a href="vim.profile.ApplyProfile.md#property">property</a>  list to access the additional configuration data.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Linkable identifier. |
| name | string | None | None | Unique identifier for the distributed virtual switch. |
| uplink | [vim.profile.host.PnicUplinkProfile](vim.profile.host.PnicUplinkProfile.md "vim.profile.host.PnicUplinkProfile") | true | None | List of subprofiles that map physical NICs to uplink ports.  Use the <a href="vim.profile.host.PnicUplinkProfile.md#key">key</a> property to access  subprofiles in the list. |


