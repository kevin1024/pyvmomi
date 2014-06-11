vim.cluster.DpmConfigInfo
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


Configuration of the VMware DPM service.   <p>   All fields are defined as optional. In case of a reconfiguration,   unset fields are not changed.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| enabled | bool | true | None | Flag indicating whether or not the service is enabled. This  service can not be enabled, unless DRS is enabled as well. |
| defaultDpmBehavior | [vim.cluster.DpmConfigInfo.DpmBehavior](vim.cluster.DpmConfigInfo.DpmBehavior.md "vim.cluster.DpmConfigInfo.DpmBehavior") | true | None | Specifies the default VMware DPM behavior for   hosts. This default behavior can be overridden on a per host   basis using the <a href="vim.cluster.DpmHostConfigInfo.md">ClusterDpmHostConfigInfo</a> object. |
| hostPowerActionRate | int | true | None | DPM generates only those recommendations that are above the   specified rating. Ratings vary from 1 to 5. This setting applies   to both manual and automated (@link DpmBehavior) DPM clusters. |
| option | [vim.option.OptionValue](vim.option.OptionValue.md "vim.option.OptionValue") | true | None | Advanced settings. |


