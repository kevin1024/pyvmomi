vim.vApp.IpPool.IpPoolConfigInfo
================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Specifications of either IPv4 or IPv6 configuration to be used   on this network. This is a part of network configuration.   <p>   IPv4 addresses are in dot-decimal notation, e.g.: 192.0.2.235   <p>   IPv6 addresses are in colon-hexadecimal notation,   e.g.: 2001:0db8:85a3::0370:7334

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| subnetAddress | string | true | None | Address of the subnet.  <p>  For example:  <ul>  <li>IPv4: 192.168.5.0</li>  <li>IPv6: 2001:0db8:85a3::</li>  </ul> |
| netmask | string | true | None | Netmask  <p>  For example:  <ul>  <li>IPv4: 255.255.255.0</li>  <li>IPv6: ffff:ffff:ffff::</li>  </ul> |
| gateway | string | true | None | Gateway. This can be an empty string - if no gateway is configured.  <p>  Examples:  <ul>  <li>IPv4: 192.168.5.1</li>  <li>IPv6: 2001:0db8:85a3::1</li>  </ul> |
| range | string | true | None | IP range. This is specified as a set of ranges separated with commas.   One range is given by a start address, a hash (#), and the length   of the range.   <p>   For example:   <ul>   <li>192.0.2.235 # 20 is the IPv4 range from 192.0.2.235 to 192.0.2.254</li>   <li>2001::7334 # 20 is the IPv6 range from 2001::7334 to 2001::7347</li>   </ul> |
| dns | string | true | None | DNS servers  <p>  For example:  <ul>  <li>IPv4: ["10.20.0.1", "10.20.0.2"]</li>  <li>IPv6: ["2001:0db8:85a3::0370:7334", "2001:0db8:85a3::0370:7335"]</li>  </ul>  <p>  If an empty list is passed, the existing value remains unchanged. To clear this  list, pass an array containing the empty string as it's only element. |
| dhcpServerAvailable | bool | true | None | Whether a DHCP server is available on this network. |
| ipPoolEnabled | bool | true | None | IP addresses can only be allocated from the range if the IP pool is   enabled. |


