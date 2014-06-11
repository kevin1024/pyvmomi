vim.profile.ProfilePropertyPath
===============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.ProfilePropertyPath.md">ProfilePropertyPath</a> data object represents  the path to a profile, policy option, or specific parameter. If <code>profilePath</code>,  <code>policyId</code>, and <code>parameterId</code> are all specified, the  combination of the three identifies a particular parameter. If only <code>profilePath</code>  and <code>policyId</code> are specified, the combination identifies a  specific profile policy option. If just the <code>profilePath</code> is  specified, the data object identifies a profile instance.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| profilePath | string | None | None | Complete path to the leaf profile, relative to the root of the host profile  document. |
| policyId | string | true | None | Policy option identifier. See <a href="vim.profile.PolicyOption.md">PolicyOption</a>.<a href="vim.profile.PolicyOption.md#id">id</a>. |
| parameterId | string | true | None | Key for a parameter in the policy specified by <code>policyId</code>.  See <a href="vim.profile.PolicyOption.md">PolicyOption</a>.<a href="vim.profile.PolicyOption.md#parameter">parameter</a>  and <a href="vmodl.KeyAnyValue.md#key">key</a>. |


