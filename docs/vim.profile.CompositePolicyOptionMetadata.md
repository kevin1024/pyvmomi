vim.profile.CompositePolicyOptionMetadata
=========================================
inherits from [vim.profile.PolicyOptionMetadata](docs/vim.profile.PolicyOptionMetadata.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.CompositePolicyOptionMetadata.md">ProfileCompositePolicyOptionMetadata</a> data object represents the metadata information  for a composite <a href="vim.profile.PolicyOption.md">PolicyOption</a>. The user will retrieve metadata  information about a composite policy and then combine policy options to produce  the composite policy option.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| option | string | None | None | List of optional policy option identifiers that could be combined  in this composite policy option. The policy options should already be  part of the possible policy options for the policy. See the  <a href="vim.profile.PolicyMetadata.md">ProfilePolicyMetadata</a>.<a href="vim.profile.PolicyMetadata.md#possibleOption">possibleOption</a>  list. |


