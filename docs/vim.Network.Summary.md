vim.Network.Summary
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


General information about a network.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| network | [vim.Network](vim.Network.md "vim.Network") | true | None | Reference to the associated managed object. |
| name | string | None | None | Name of the network. |
| accessible | bool | None | None | At least one host is configured to provide this network. |
| ipPoolName | string | None | None | Name of the associated IP pool. Empty if the network is not associated with an  IP pool. |
| ipPoolId | int | true | None | Identifier of the associated IP pool. Zero if the network is not associated  with an IP pool. |


