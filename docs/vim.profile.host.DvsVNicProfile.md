vim.profile.host.DvsVNicProfile
===============================
inherits from [vim.profile.ApplyProfile](docs/vim.profile.ApplyProfile.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.host.DvsVNicProfile.md">DvsVNicProfile</a> data object is the base object  for host and service console Virtual NIC subprofiles.  If a profile plug-in defines additional policies or subprofiles, use the  <a href="vim.profile.ApplyProfile.md#policy">policy</a> or <a href="vim.profile.ApplyProfile.md#property">property</a>  list to access the configuration data.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Linkable identifier. |
| ipConfig | [vim.profile.host.IpAddressProfile](vim.profile.host.IpAddressProfile.md "vim.profile.host.IpAddressProfile") | None | None | IP address for a distributed virtual switch Virtual NIC. |


