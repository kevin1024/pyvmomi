vim.vm.DefinedProfileSpec
=========================
inherits from [vim.vm.ProfileSpec](docs/vim.vm.ProfileSpec.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


Policy specification that carries a pre-defined Storage Policy to be associated   with a Virtual Machine Home or a Virtual Disk object. Such a pre-defined   policy can be either be vSphere Storage Administrator defined or may come   from a set of pre-defined policies from Storage Vendor.    <p>   Neither the association nor the policy data is persisted in Virtual Machine   configuration. This data is managed by the an extension of Virtual Center   (Storage Policy Based Management).   <p>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| profileId | string | None | None | Storage Policy Profile identification - Should be  pbm.profileId but for implementation reasons, could not be. |
| profileData | [vim.vm.ProfileRawData](vim.vm.ProfileRawData.md "vim.vm.ProfileRawData") | true | None | Profile data sent to the Storage Backend by vSphere.   <p>   This data is provided by the SPBM component of the vSphere platform.   This field should not be set by Virtual Center users. |


