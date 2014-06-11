vim.dvs.VmwareDistributedVirtualSwitch.MtuHealthCheckResult
===========================================================
inherits from [vim.dvs.HostMember.UplinkHealthCheckResult](docs/vim.dvs.HostMember.UplinkHealthCheckResult.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


This class defines MTU health check result of an uplink port   in the VMware vSphered Distributed Switch.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| mtuMismatch | bool | None | None | True if the MTU configured in the vSphere Distributed Switch is different from   the value configured in the Physical NIC, else false. If it is true,   MTU health check is stopped. In this case, <a href="vim.dvs.VmwareDistributedVirtualSwitch.MtuHealthCheckResult.md#vlanSupportSwitchMtu">vlanSupportSwitchMtu</a> and   <a href="vim.dvs.VmwareDistributedVirtualSwitch.MtuHealthCheckResult.md#vlanNotSupportSwitchMtu">vlanNotSupportSwitchMtu</a> will not have values. |
| vlanSupportSwitchMtu | [vim.NumericRange](vim.NumericRange.md "vim.NumericRange") | true | None | The vlan's MTU setting on physical switch allows vSphere Distributed Switch   max MTU size packets passing.   If the vlan is not a range, but a single Id,   both start and end have the same value with the single vlan Id. |
| vlanNotSupportSwitchMtu | [vim.NumericRange](vim.NumericRange.md "vim.NumericRange") | true | None | The vlan's MTU setting on physical switch does not allow   vSphere Distributed Switch max MTU size packets passing.   If the vlan is not a range, but a single Id,   both start and end have the same value with the single vlan Id. |


