vim.profile.PolicyOptionMetadata
================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.PolicyOptionMetadata.md">ProfilePolicyOptionMetadata</a> data object contains the metadata information  for a <a href="vim.profile.PolicyOption.md">PolicyOption</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | [vim.ExtendedElementDescription](vim.ExtendedElementDescription.md "vim.ExtendedElementDescription") | None | None | Identifier for the policy option.  <ul>  <li>The <code>id.key</code> value  (<a href="vim.ExtendedElementDescription.md">ExtendedElementDescription</a>.<a href="vim.ElementDescription.md#key">key</a>)  identifies the policy option type.</li>  <li>The <code>id.label</code> property  (<a href="vim.ExtendedElementDescription.md">ExtendedElementDescription</a>.<a href="vim.Description.md#label">label</a>)  contains a brief localizable message describing the policy option.</li>  <li>The <code>id.summary</code> property  (<a href="vim.ExtendedElementDescription.md">ExtendedElementDescription</a>.<a href="vim.Description.md#summary">summary</a>)  contains a localizable summary of the policy option.  Summary information can contain embedded variable names which can  be replaced with values from the <code>parameter</code> property.</li> |
| parameter | [vim.profile.ParameterMetadata](vim.profile.ParameterMetadata.md "vim.profile.ParameterMetadata") | true | None | Metadata about the parameters for the policy option. |


