vim.host.PortGroup.Specification
================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes the PortGroup specification    representing the properties on a PortGroup that   can be configured.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | The name of the port group. |
| vlanId | int | None | None | The VLAN ID for ports using this port group. Possible values:   <ul>   <li>A value of 0 specifies that you do not want the port group associated   with a VLAN.   <li>A value from 1 to 4094 specifies a VLAN ID for the port group.   <li>A value of 4095 specifies that the port group should use trunk mode,   which allows the guest operating system to manage its own VLAN tags. |
| vswitchName | string | None | None | The identifier of the virtual switch on which   this port group is located. |
| policy | [vim.host.NetworkPolicy](vim.host.NetworkPolicy.md "vim.host.NetworkPolicy") | None | None | Policies on the port group take precedence over the ones specified   on the virtual switch. |


