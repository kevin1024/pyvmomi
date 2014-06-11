vim.cluster.InitialPlacementAction
==================================
inherits from [vim.cluster.Action](docs/vim.cluster.Action.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


Describes an initial placement of a single virtual machine

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| targetHost | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | None | None | The host where the virtual machine should be initially placed. |
| pool | [vim.ResourcePool](vim.ResourcePool.md "vim.ResourcePool") | true | None | The resource pool to place the virtual machine into in case this        action is for migrating from outside cluster. |


