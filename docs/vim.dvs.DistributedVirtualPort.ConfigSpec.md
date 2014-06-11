vim.dvs.DistributedVirtualPort.ConfigSpec
=========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Specification to reconfigure a <a href="vim.dvs.DistributedVirtualPort.md">DistributedVirtualPort</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| operation | string | None | None | The operation to remove or modify the existing ports. The valid values   are:   <ul>     <li><a href="vim.ConfigSpecOperation.md#edit">edit</a></li>     <li><a href="vim.ConfigSpecOperation.md#remove">remove</a></li>   </ul> |
| key | string | true | None | Key of the port to be reconfigured. |
| name | string | true | None | The name of the port. |
| scope | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | true | None | The eligible entities that can connect to the port, for detail see   <a href="vim.dvs.DistributedVirtualPort.ConfigInfo.md#scope">scope</a>. |
| description | string | true | None | The description string of the port. |
| setting | [vim.dvs.DistributedVirtualPort.Setting](vim.dvs.DistributedVirtualPort.Setting.md "vim.dvs.DistributedVirtualPort.Setting") | true | None | The network setting of the port. |
| configVersion | string | true | None | The version string of the configuration. |


