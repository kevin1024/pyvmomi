vim.vm.customization.IPSettings
===============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


IP settings for a virtual network adapter.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ip | [vim.vm.customization.IpGenerator](vim.vm.customization.IpGenerator.md "vim.vm.customization.IpGenerator") | None | None | Specification to obtain a unique IP address for this virtual network adapter. |
| subnetMask | string | true | None | Subnet mask for this virtual network adapter. |
| gateway | string | true | None | For a virtual network adapter with a static IP address, this data object type   contains a list of gateways, in order of preference. |
| ipV6Spec | [vim.vm.customization.IPSettings.IpV6AddressSpec](vim.vm.customization.IPSettings.IpV6AddressSpec.md "vim.vm.customization.IPSettings.IpV6AddressSpec") | true | None | This contains the IpGenerator, subnet mask and gateway info for all   the ipv6 addresses associated with the virtual network adapter. |
| dnsServerList | string | true | None | A list of server IP addresses to use for DNS lookup in a Windows guest operating   system. In Windows, these settings are adapter-specific, whereas in Linux, they   are global. As a result, the Linux guest customization process ignores this   setting and looks for its DNS servers in the globalIPSettings object.   <p>   Specify these servers in order of preference. If this list is not empty, and if   a DHCP IpGenerator is used, then these settings override the DHCP settings. |
| dnsDomain | string | true | None | A DNS domain suffix such as vmware.com. |
| primaryWINS | string | true | None | The IP address of the primary WINS server. This property is ignored for Linux   guest operating systems. |
| secondaryWINS | string | true | None | The IP address of the secondary WINS server. This property is ignored for Linux   guest operating systems. |
| netBIOS | [vim.vm.customization.IPSettings.NetBIOSMode](vim.vm.customization.IPSettings.NetBIOSMode.md "vim.vm.customization.IPSettings.NetBIOSMode") | true | None | NetBIOS setting for Windows. |


