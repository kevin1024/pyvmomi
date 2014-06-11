vim.host.PortGroup
==================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type is used to describe port groups.   Port groups are used to group virtual network adapters on a virtual switch,   associating them with networks and network policies.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | true | None | The linkable identifier. |
| port | [vim.host.PortGroup.Port](vim.host.PortGroup.Port.md "vim.host.PortGroup.Port") | true | None | The ports that currently exist and are used on this port group. |
| vswitch | [vim.host.VirtualSwitch](vim.host.VirtualSwitch.md "vim.host.VirtualSwitch") | true | None | The virtual switch that contains this port group. |
| computedPolicy | [vim.host.NetworkPolicy](vim.host.NetworkPolicy.md "vim.host.NetworkPolicy") | None | None | Computed network policies that are applicable for a port group.  The   inheritance scheme for PortGroup requires knowledge about the   NetworkPolicy for a port group and its parent virtual switch as well as   the logic for computing the results.  This information is provided as   a convenience so that callers need not duplicate the inheritance logic   to determine the proper values for a network policy.   <p>   See the description of the    <a href="vim.host.NetworkPolicy.md">NetworkPolicy</a> data object type   for more information. |
| spec | [vim.host.PortGroup.Specification](vim.host.PortGroup.Specification.md "vim.host.PortGroup.Specification") | None | None | The specification of a port group. |


