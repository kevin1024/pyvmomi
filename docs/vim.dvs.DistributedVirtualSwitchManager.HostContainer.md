vim.dvs.DistributedVirtualSwitchManager.HostContainer
=====================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Check host compatibility for all hosts in the container. If the recursive  flag is true, then check hosts at all levels within this container, otherwise  check only at the container level. In case of container being a <a href="vim.Datacenter.md">Datacenter</a>,  the recursive flag is applied to its HostFolder.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| container | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | None | None | Check compatibility of hosts in this container. The supported container  types are Datacenter, Folder, and ComputeResource. |
| recursive | bool | None | None | If true, include hosts of all levels in the hierarchy with  container as root of the tree. In case of container being a <a href="vim.Datacenter.md">Datacenter</a>,  the recursive flag is applied to its HostFolder. |


