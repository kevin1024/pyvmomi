vim.dvs.VmwareDistributedVirtualSwitch.VlanIdSpec
=================================================
inherits from [vim.dvs.VmwareDistributedVirtualSwitch.VlanSpec](docs/vim.dvs.VmwareDistributedVirtualSwitch.VlanSpec.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data type defines the configuration when single vlanId is used for  the port.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vlanId | int | None | None | The VLAN ID for ports. Possible values:   <ul>   <li>A value of 0 specifies that you do not want the port associated   with a VLAN.   <li>A value from 1 to 4094 specifies a VLAN ID for the port. |


