vim.profile.host.StorageProfile
===============================
inherits from [vim.profile.ApplyProfile](docs/vim.profile.ApplyProfile.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.host.StorageProfile.md">StorageProfile</a> data object represents the host storage configuration.  If a profile plug-in defines policies or subprofiles, use the  <a href="vim.profile.ApplyProfile.md#policy">policy</a> or <a href="vim.profile.ApplyProfile.md#property">property</a>  list to access the additional configuration data.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| nasStorage | [vim.profile.host.NasStorageProfile](vim.profile.host.NasStorageProfile.md "vim.profile.host.NasStorageProfile") | true | None | List of NAS storage subprofiles. Use the <a href="vim.profile.host.NasStorageProfile.md#key">key</a> property  to access a subprofile in the list. |


