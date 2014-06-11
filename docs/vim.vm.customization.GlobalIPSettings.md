vim.vm.customization.GlobalIPSettings
=====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


A collection of global IP settings for a virtual network adapter. In Linux, DNS   server settings are global. The settings can either be statically set or supplied   by a DHCP server.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| dnsSuffixList | string | true | None | List of name resolution suffixes for the virtual network adapter. This list   applies to both Windows and Linux guest customization. For Linux, this setting   is global, whereas in Windows, this setting is listed on a per-adapter basis,   even though the setting is global in Windows. |
| dnsServerList | string | true | None | List of DNS servers, for a virtual network adapter with a static IP address. If   this list is empty, then the guest operating system is expected to use a DHCP   server to get its DNS server settings. These settings configure the virtual   machine to use the specified DNS servers. These DNS server settings are listed   in order of preference. |


