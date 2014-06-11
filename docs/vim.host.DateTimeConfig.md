vim.host.DateTimeConfig
=======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This data object represents the dateTime configuration of the host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| timeZone | string | true | None | The time zone of the host.    Must be one of the values of    <a href="vim.host.DateTimeSystem.TimeZone.md#key">key</a> |
| ntpConfig | [vim.host.NtpConfig](vim.host.NtpConfig.md "vim.host.NtpConfig") | true | None | The NTP configuration on the host. |


