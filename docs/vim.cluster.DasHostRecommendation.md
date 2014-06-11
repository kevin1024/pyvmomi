vim.cluster.DasHostRecommendation
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


A host recommendation for a virtual machine managed by the VMware   HA Service.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| host | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | None | None | The recommended host. |
| drsRating | int | true | None | Rating as computed by DRS for a DRS-enabled cluster. Rating    range from 1 to 5, and the higher the rating, the stronger DRS    suggests this host is picked for the operation. |


