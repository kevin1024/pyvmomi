vim.profile.cluster.ClusterProfile.ConfigServiceCreateSpec
==========================================================
inherits from [vim.profile.cluster.ClusterProfile.ConfigSpec](docs/vim.profile.cluster.ClusterProfile.ConfigSpec.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


DataObject which allows reconfiguration of a profile  based on services that will be available on the cluster.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| serviceType | string | true | None | Type of the service for which the ClusterProfile is being requested.  If more than one service is specified, the created ClusterProfile  will cater for all the services.  Possible values are specified by   <a href="vim.profile.cluster.ClusterProfile.ServiceType.md">ClusterProfileServiceType</a>.  If unset, clear the compliance expressions on the profile. |


