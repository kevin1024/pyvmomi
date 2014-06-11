vim.profile.PolicyOption
========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.PolicyOption.md">PolicyOption</a> data object represents one or more configuration   values. A policy option is one of the configuration options from the   <a href="vim.profile.PolicyMetadata.md">ProfilePolicyMetadata</a>.<a href="vim.profile.PolicyMetadata.md#possibleOption">possibleOption</a>   list.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | string | None | None | Identifier for the policy option. This value matches one of the   keys from the list of possible options in the policy metadata   (<a href="vim.profile.PolicyMetadata.md">ProfilePolicyMetadata</a>.<a href="vim.profile.PolicyMetadata.md#possibleOption">possibleOption</a>[].<a href="vim.profile.PolicyOptionMetadata.md#id">id</a>.<a href="vim.ElementDescription.md#key">key</a>). |
| parameter | [vmodl.KeyAnyValue](vmodl.KeyAnyValue.md "vmodl.KeyAnyValue") | true | None | Parameters for the policy option.   This list must include all parameters that are not marked as optional   in the policy option metadata parameter list   (<a href="vim.profile.PolicyMetadata.md">ProfilePolicyMetadata</a>.<a href="vim.profile.PolicyMetadata.md#possibleOption">possibleOption</a>[].<a href="vim.profile.PolicyOptionMetadata.md#parameter">parameter</a>[].<a href="vim.profile.ParameterMetadata.md#optional">optional</a>). |


