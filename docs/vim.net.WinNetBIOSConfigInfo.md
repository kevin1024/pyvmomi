vim.net.WinNetBIOSConfigInfo
============================
inherits from [vim.net.NetBIOSConfigInfo](docs/vim.net.NetBIOSConfigInfo.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


This data object type describes the Windows-specific  NetBIOS configuration.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| primaryWINS | string | None | None | The IP address of the primary WINS server. |
| secondaryWINS | string | true | None | The IP address of the secondary WINS server. |


