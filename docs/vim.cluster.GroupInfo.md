vim.cluster.GroupInfo
=====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


<a href="vim.cluster.GroupInfo.md">ClusterGroupInfo</a> is the base type for all virtual machine    and host groups. All virtual machines and hosts that are part of a group    must be part of the same cluster.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | Unique name of the group. |
| userCreated | bool | true | None | Flag to indicate whether the group is created by the user or the system. |


