vim.profile.host.HostProfile.SerializedHostProfileSpec
======================================================
inherits from [vim.profile.Profile.SerializedCreateSpec](docs/vim.profile.Profile.SerializedCreateSpec.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


The <a href="vim.profile.host.HostProfile.SerializedHostProfileSpec.md">HostProfileSerializedHostProfileSpec</a> data object  contains a string representation of a host profile. Use this object when you  create a host profile from a file.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| validatorHost | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | true | None | Host for profile validation. This can be a host on which  the profile is intended to be used. |


