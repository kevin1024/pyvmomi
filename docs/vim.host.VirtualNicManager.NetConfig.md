vim.host.VirtualNicManager.NetConfig
====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The NetConfig data object type contains the networking   configuration.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| nicType | string | None | None | The NicType of this NetConfig. |
| multiSelectAllowed | bool | None | None | Whether multiple nics can be selected for this nicType. |
| candidateVnic | [vim.host.VirtualNic](vim.host.VirtualNic.md "vim.host.VirtualNic") | true | None | List of VirtualNic objects that may be used.   This will be a subset of the list of VirtualNics in   <a href="vim.host.NetworkInfo.md#vnic">vnic</a>. |
| selectedVnic | [vim.host.VirtualNic](vim.host.VirtualNic.md "vim.host.VirtualNic") | true | None | List of VirtualNic objects that are selected for use. |


