vim.cluster.HostRecommendation
==============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


A DRS recommended host for either powering on, resuming or  reverting a virtual machine, or migrating a virtual machine from  outside the cluster.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| host | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | None | None | The recommended host. |
| rating | int | None | None | Rating for the recommendation. Ratings range from 1 to 5, and   the higher the rating, the stronger DRS suggests this host is   picked for the operation. |


