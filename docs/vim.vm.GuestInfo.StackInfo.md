vim.vm.GuestInfo.StackInfo
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Information about the Internet Protocol stack   as configured in the guest operating system.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| dnsConfig | [vim.net.DnsConfigInfo](vim.net.DnsConfigInfo.md "vim.net.DnsConfigInfo") | true | None | Client DNS configuration. How DNS queries are resolved. |
| ipRouteConfig | [vim.net.IpRouteConfigInfo](vim.net.IpRouteConfigInfo.md "vim.net.IpRouteConfigInfo") | true | None | IP route table configuration. |
| ipStackConfig | [vim.KeyValue](vim.KeyValue.md "vim.KeyValue") | true | None | Report Kernel IP configuration settings.  The key part contains a unique number in the report.  The value part contains the 'key=value'  as provided by the underlying provider.  For example on Linux, BSD, the  systcl -a output would be reported as:    key='5', value='net.ipv4.tcp_keepalive_time = 7200' |
| dhcpConfig | [vim.net.DhcpConfigInfo](vim.net.DhcpConfigInfo.md "vim.net.DhcpConfigInfo") | true | None | Client side DHCP for a given interface.  This reports only the system wide dhcp client settings.  See NicInfo.IpConfig for per interface settings.  For example on Linux, BSD systems:  Using the file dhclient.conf output would be reported as:    key='1', value='timeout 60;'    key='2', value='reboot 10;' |


