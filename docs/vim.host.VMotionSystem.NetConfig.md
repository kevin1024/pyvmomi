vim.host.VMotionSystem.NetConfig
================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The NetConfig data object type contains the networking   configuration for VMotion operations.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| candidateVnic | [vim.host.VirtualNic](vim.host.VirtualNic.md "vim.host.VirtualNic") | true | None | List of VirtualNic objects that may be used for VMotion.   This will be a subset of the list of VirtualNics in   <a href="vim.host.NetworkInfo.md#vnic">vnic</a>. |
| selectedVnic | [vim.host.VirtualNic](vim.host.VirtualNic.md "vim.host.VirtualNic") | true | None | VirtualNic that is selected for use in VMotion operations. |


