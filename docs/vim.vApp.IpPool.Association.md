vim.vApp.IpPool.Association
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Information about a network or portgroup that is associated to an IP pool.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| network | [vim.Network](vim.Network.md "vim.Network") | true | System.Read | The network object |
| networkName | string | None | None | The name of the network or portgroup  <p>  This field is only used when querying existing IP pools. It is ignored when  creating or updating pools. |


