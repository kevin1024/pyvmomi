vim.profile.PolicyMetadata
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.PolicyMetadata.md">ProfilePolicyMetadata</a> data object represents the metadata information  for a <a href="vim.profile.Policy.md">ProfilePolicy</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | [vim.ExtendedElementDescription](vim.ExtendedElementDescription.md "vim.ExtendedElementDescription") | None | None | Identifier for the policy. |
| possibleOption | [vim.profile.PolicyOptionMetadata](vim.profile.PolicyOptionMetadata.md "vim.profile.PolicyOptionMetadata") | None | None | Possible policy options that can be set for a policy of the   given kind. <a href="vim.profile.host.HostProfile.md">HostProfile</a>s and subprofiles   will contain selected policy options from this list. See   <a href="vim.profile.PolicyOption.md">PolicyOption</a>. |


