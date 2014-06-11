vim.dvs.VmwareDistributedVirtualSwitch.VlanHealthCheckResult
============================================================
inherits from [vim.dvs.HostMember.UplinkHealthCheckResult](docs/vim.dvs.HostMember.UplinkHealthCheckResult.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


This class defines Vlan health check result of an uplink port   in the VMware vSphered Distributed Switch.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| trunkedVlan | [vim.NumericRange](vim.NumericRange.md "vim.NumericRange") | true | None | The vlans which are trunked by the physical switch connected to the uplink port.   If the vlan is not a range, but a single Id,   both start and end have the same value with the single vlan Id. |
| untrunkedVlan | [vim.NumericRange](vim.NumericRange.md "vim.NumericRange") | true | None | The vlans which are not trunked by the physical switch connected to the uplink port.   If the vlan is not a range, but a single Id,   both start and end have the same value with the single vlan Id. |


