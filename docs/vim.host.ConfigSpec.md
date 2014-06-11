vim.host.ConfigSpec
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.host.ConfigSpec.md">HostConfigSpec</a> data object provides access to data objects   that specify configuration changes to be applied to an ESX host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| nasDatastore | [vim.host.NasVolume.Config](vim.host.NasVolume.Config.md "vim.host.NasVolume.Config") | true | None | Configurations to create NAS datastores. |
| network | [vim.host.NetworkConfig](vim.host.NetworkConfig.md "vim.host.NetworkConfig") | true | None | Network system information. |
| nicTypeSelection | [vim.host.VirtualNicManager.NicTypeSelection](vim.host.VirtualNicManager.NicTypeSelection.md "vim.host.VirtualNicManager.NicTypeSelection") | true | None | Type selection for different VirtualNics. |
| service | [vim.host.ServiceConfig](vim.host.ServiceConfig.md "vim.host.ServiceConfig") | true | None | Host service configuration. |
| firewall | [vim.host.FirewallConfig](vim.host.FirewallConfig.md "vim.host.FirewallConfig") | true | None | Firewall configuration. |
| option | [vim.option.OptionValue](vim.option.OptionValue.md "vim.option.OptionValue") | true | None | Host configuration options as defined by the   <a href="vim.option.OptionValue.md">OptionValue</a> data object type. |
| datastorePrincipal | string | true | None | Datastore principal user. |
| datastorePrincipalPasswd | string | true | None | Password for the datastore principal. |
| datetime | [vim.host.DateTimeConfig](vim.host.DateTimeConfig.md "vim.host.DateTimeConfig") | true | None | DateTime Configuration. |
| storageDevice | [vim.host.StorageDeviceInfo](vim.host.StorageDeviceInfo.md "vim.host.StorageDeviceInfo") | true | None | Storage system information. |
| license | [vim.host.LicenseSpec](vim.host.LicenseSpec.md "vim.host.LicenseSpec") | true | None | License configuration for the host. |
| security | [vim.host.SecuritySpec](vim.host.SecuritySpec.md "vim.host.SecuritySpec") | true | None | Security specification. |
| userAccount | [vim.host.LocalAccountManager.AccountSpecification](vim.host.LocalAccountManager.AccountSpecification.md "vim.host.LocalAccountManager.AccountSpecification") | true | None | List of users to create/update with new password. |
| usergroupAccount | [vim.host.LocalAccountManager.AccountSpecification](vim.host.LocalAccountManager.AccountSpecification.md "vim.host.LocalAccountManager.AccountSpecification") | true | None | List of users to create/update with new password. |
| memory | [vim.host.MemorySpec](vim.host.MemorySpec.md "vim.host.MemorySpec") | true | None | Memory configuration for the host. |
| activeDirectory | [vim.host.ActiveDirectorySpec](vim.host.ActiveDirectorySpec.md "vim.host.ActiveDirectorySpec") | true | None | Active Directory configuration change. |
| genericConfig | [vmodl.KeyAnyValue](vmodl.KeyAnyValue.md "vmodl.KeyAnyValue") | true | None | Advanced configuration. |


