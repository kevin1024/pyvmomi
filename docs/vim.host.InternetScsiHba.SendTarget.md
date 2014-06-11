vim.host.InternetScsiHba.SendTarget
===================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The iSCSI send target.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| address | string | None | None | The IP address or hostname of the storage device. |
| port | int | true | None | The TCP port of the storage device.  If not specified, the standard default of 3260 is used. |
| authenticationProperties | [vim.host.InternetScsiHba.AuthenticationProperties](vim.host.InternetScsiHba.AuthenticationProperties.md "vim.host.InternetScsiHba.AuthenticationProperties") | true | None | The authentication settings for this discovery target.    All static targets discovered via this target will inherit the   use of these settings unless the static target's authentication   settings are explicitly set. |
| digestProperties | [vim.host.InternetScsiHba.DigestProperties](vim.host.InternetScsiHba.DigestProperties.md "vim.host.InternetScsiHba.DigestProperties") | true | None | The digest settings for this discovery target.    All static targets discovered via this target will inherit the   use of these settings unless the static target's digest   settings are explicitly set. |
| supportedAdvancedOptions | [vim.option.OptionDef](vim.option.OptionDef.md "vim.option.OptionDef") | true | None | A list of supported key/value pair advanced options for the   host bus adapter including their type information. |
| advancedOptions | [vim.host.InternetScsiHba.ParamValue](vim.host.InternetScsiHba.ParamValue.md "vim.host.InternetScsiHba.ParamValue") | true | None | A list of the current options settings for the host bus adapter. |
| parent | string | true | None | The device name of the host bus adapter from which settings   can be inherited. |


