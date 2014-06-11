vim.dvs.VmwareDistributedVirtualSwitch.TrunkVlanSpec
====================================================
inherits from [vim.dvs.VmwareDistributedVirtualSwitch.VlanSpec](docs/vim.dvs.VmwareDistributedVirtualSwitch.VlanSpec.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data type specifies that the port uses trunk mode,  which allows the guest operating system to manage its own VLAN tags.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vlanId | [vim.NumericRange](vim.NumericRange.md "vim.NumericRange") | None | None | The VlanId range for the trunk port. The valid VlanId range is   from 0 to 4094. Overlapping ranges are allowed. |


