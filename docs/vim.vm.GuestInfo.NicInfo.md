vim.vm.GuestInfo.NicInfo
========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| network | string | true | None | Name of the virtual switch portgroup or dvPort connected to this adapter. |
| ipAddress | string | true | None |  |
| macAddress | string | true | None | MAC address of the adapter. |
| connected | bool | None | None | Flag indicating whether or not the virtual device is connected. |
| deviceConfigId | int | None | None | Link to the corresponding virtual device. |
| dnsConfig | [vim.net.DnsConfigInfo](vim.net.DnsConfigInfo.md "vim.net.DnsConfigInfo") | true | None | DNS configuration of the adapter.  This property is set only when Guest OS supports it.  See StackInfo dnsConfig for system wide  settings. |
| ipConfig | [vim.net.IpConfigInfo](vim.net.IpConfigInfo.md "vim.net.IpConfigInfo") | true | None | IP configuration settings of the adapter  See StackInfo ipStackConfig for system wide  settings. |
| netBIOSConfig | [vim.net.NetBIOSConfigInfo](vim.net.NetBIOSConfigInfo.md "vim.net.NetBIOSConfigInfo") | true | None | NetBIOS configuration of the adapter |


