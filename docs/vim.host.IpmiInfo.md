vim.host.IpmiInfo
=================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The IpmiInfo data object contains IPMI (Intelligent Platform Management Interface)    and BMC (Baseboard Management Controller) information for the host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| bmcIpAddress | string | true | None | IP address of the BMC on the host. It should be null terminated. |
| bmcMacAddress | string | true | None | MAC address of the BMC on the host. The MAC address should be of the    form xx:xx:xx:xx:xx:xx where each x is a hex digit. It should be null   terminated. |
| login | string | true | None | User ID for logging into the BMC. BMC usernames may be up to 16    characters and must be null terminated. Hence, a login comprises    17 or fewer characters. |
| password | string | true | None | Password for logging into the BMC. Only used for configuration, returned as unset    while reading. The password can be up to 16 characters and must be null   terminated. Hence, a password comprises 17 or fewer characters. |


