vim.host.DhcpService.Specification
==================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| virtualSwitch | string | None | None | The name of the virtual switch to which DHCP service is connected. |
| defaultLeaseDuration | int | None | None | The default DHCP lease duration (minutes). |
| leaseBeginIp | string | None | None | The start of the IP address range served by the DHCP service. |
| leaseEndIp | string | None | None | The end of the IP address range served by the DHCP service. |
| maxLeaseDuration | int | None | None | The maximum DHCP lease duration (minutes). |
| unlimitedLease | bool | None | None | A flag to indicate whether or not unlimited DHCP lease    durations are allowed. |
| ipSubnetAddr | string | None | None | Subnet served by DHCP service. |
| ipSubnetMask | string | None | None | Subnet mask of network served by DHCP service. |


