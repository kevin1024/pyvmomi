vim.profile.cluster.ClusterProfile.CompleteConfigSpec
=====================================================
inherits from [vim.profile.cluster.ClusterProfile.ConfigSpec](docs/vim.profile.cluster.ClusterProfile.ConfigSpec.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


DataObject completely specifying the configuration of   the profile.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| complyProfile | [vim.profile.ComplianceProfile](vim.profile.ComplianceProfile.md "vim.profile.ComplianceProfile") | true | None | User defined compliance profile for the cluster.  If unset, clear the complyProfile. |


