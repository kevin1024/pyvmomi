vim.host.PhysicalNic.CdpInfo
============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


CDP (Cisco Discovery Protocol) is a link level protocol that allows    for discovering the CDP-awared network hardware at either end of a    DIRECT connection. It's only good for direct connection because CDP    doesn't get forwarded through switches.     It's a simple advertisement protocol which beacons information about    the switch or host along with some port information. The CDP information    allows ESX Server admins to know which Cisco switch port is connected to    any given virtual switch uplink (PNIC).

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| cdpVersion | int | true | None | CDP version. The value is always 1. |
| timeout | int | true | None | This is the periodicity of advertisement, the time between two    successive CDP message transmissions |
| ttl | int | true | None | Time-To-Live.  the amount of time, in seconds, that a receiver should    retain the information contained in the CDP packet. |
| samples | int | true | None | The number of CDP messages we have received from the device. |
| devId | string | true | None | Device ID which identifies the device. By default, the device ID is    either the device's fully-qualified host name (including the domain    name) or the device's hardware serial number in ASCII. |
| address | string | true | None | The advertised IP address that is assigned to the interface of the device    on which the CDP message is sent. The device can advertise all addresses for    a given protocol suite and, optionally, can advertise one or more loopback    IP addresses. But this property only show the first address. |
| portId | string | true | None | Port ID. An ASCII character string that identifies the port on which    the CDP message is sent, e.g. "FastEthernet0/8" |
| deviceCapability | [vim.host.PhysicalNic.CdpDeviceCapability](vim.host.PhysicalNic.CdpDeviceCapability.md "vim.host.PhysicalNic.CdpDeviceCapability") | true | None | Device Capability   <a href="vim.host.PhysicalNic.CdpDeviceCapability.md">PhysicalNicCdpDeviceCapability</a> |
| softwareVersion | string | true | None | Software version on the device. A character string that provides    information about the software release version that the device is    running. e.g. "Cisco Internetwork Operating Syscisco WS-C2940-8TT-S" |
| hardwarePlatform | string | true | None | Hardware platform. An ASCII character string that describes the     hardware platform of the device , e.g. "cisco WS-C2940-8TT-S" |
| ipPrefix | string | true | None | IP prefix. Each IP prefix represents one of the directly connected    IP network segments of the local route. |
| ipPrefixLen | int | true | None | ipPrefix length. |
| vlan | int | true | None | The native VLAN of advertising port. The native VLAN is the VLAN to    which a port returns when it is not trunking. Also, the native VLAN    is the untagged VLAN on an 802.1Q trunk. |
| fullDuplex | bool | true | None | Half/full duplex setting of the advertising port. |
| mtu | int | true | None | MTU, the maximum transmission unit for the advertising port. Possible    values are 1500 through 18190. |
| systemName | string | true | None | The configured SNMP system name of the device. |
| systemOID | string | true | None | The configured SNMP system OID of the device. |
| mgmtAddr | string | true | None | The configured IP address of the SNMP management interface for the    device. |
| location | string | true | None | The configured location of the device. |


