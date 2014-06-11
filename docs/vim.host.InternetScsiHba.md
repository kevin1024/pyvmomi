vim.host.InternetScsiHba
========================
inherits from [vim.host.HostBusAdapter](docs/vim.host.HostBusAdapter.md)


This data object type describes the iSCSI host bus adapter    interface.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| isSoftwareBased | bool | None | None | True if this host bus adapter is a software based initiator   utilizing the hosting system's existing TCP/IP network connection |
| canBeDisabled | bool | true | None | Can this adapter be disabled |
| networkBindingSupport | [vim.host.InternetScsiHba.NetworkBindingSupportType](vim.host.InternetScsiHba.NetworkBindingSupportType.md "vim.host.InternetScsiHba.NetworkBindingSupportType") | true | None | Specifies if this iSCSI Adapter requires a bound network  interface to function. |
| discoveryCapabilities | [vim.host.InternetScsiHba.DiscoveryCapabilities](vim.host.InternetScsiHba.DiscoveryCapabilities.md "vim.host.InternetScsiHba.DiscoveryCapabilities") | None | None | The discovery capabilities for this host bus adapter. |
| discoveryProperties | [vim.host.InternetScsiHba.DiscoveryProperties](vim.host.InternetScsiHba.DiscoveryProperties.md "vim.host.InternetScsiHba.DiscoveryProperties") | None | None | The discovery settings for this host bus adapter. |
| authenticationCapabilities | [vim.host.InternetScsiHba.AuthenticationCapabilities](vim.host.InternetScsiHba.AuthenticationCapabilities.md "vim.host.InternetScsiHba.AuthenticationCapabilities") | None | None | The authentication capabilities for this host bus adapter. |
| authenticationProperties | [vim.host.InternetScsiHba.AuthenticationProperties](vim.host.InternetScsiHba.AuthenticationProperties.md "vim.host.InternetScsiHba.AuthenticationProperties") | None | None | The authentication settings for this host bus adapter.    All static and discovery targets will inherit the use of these   settings unless their authentication settings are explicitly set. |
| digestCapabilities | [vim.host.InternetScsiHba.DigestCapabilities](vim.host.InternetScsiHba.DigestCapabilities.md "vim.host.InternetScsiHba.DigestCapabilities") | true | None | The authentication capabilities for this host bus adapter. |
| digestProperties | [vim.host.InternetScsiHba.DigestProperties](vim.host.InternetScsiHba.DigestProperties.md "vim.host.InternetScsiHba.DigestProperties") | true | None | The digest settings for this host bus adapter.    All static and discovery targets will inherit the use of these   properties unless their digest settings are explicitly set. |
| ipCapabilities | [vim.host.InternetScsiHba.IPCapabilities](vim.host.InternetScsiHba.IPCapabilities.md "vim.host.InternetScsiHba.IPCapabilities") | None | None | The IP capabilities for this host bus adapter. |
| ipProperties | [vim.host.InternetScsiHba.IPProperties](vim.host.InternetScsiHba.IPProperties.md "vim.host.InternetScsiHba.IPProperties") | None | None | The IP settings for this host bus adapter. |
| supportedAdvancedOptions | [vim.option.OptionDef](vim.option.OptionDef.md "vim.option.OptionDef") | true | None | A list of supported key/value pair advanced options for the   host bus adapter including their type information. |
| advancedOptions | [vim.host.InternetScsiHba.ParamValue](vim.host.InternetScsiHba.ParamValue.md "vim.host.InternetScsiHba.ParamValue") | true | None | A list of the current options settings for the host bus adapter. |
| iScsiName | string | None | None | The iSCSI name of this host bus adapter. |
| iScsiAlias | string | true | None | The iSCSI alias of this host bus adapter. |
| configuredSendTarget | [vim.host.InternetScsiHba.SendTarget](vim.host.InternetScsiHba.SendTarget.md "vim.host.InternetScsiHba.SendTarget") | true | None | The configured iSCSI send target entries. |
| configuredStaticTarget | [vim.host.InternetScsiHba.StaticTarget](vim.host.InternetScsiHba.StaticTarget.md "vim.host.InternetScsiHba.StaticTarget") | true | None | The configured iSCSI static target entries. |
| maxSpeedMb | int | true | None | The maximum supported link speed of the port in megabits per second. |
| currentSpeedMb | int | true | None | The Current operating link speed of the port in megabits per second. |


