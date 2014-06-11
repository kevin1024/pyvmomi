vim.event.CustomizationSysprepFailed
====================================
inherits from [vim.event.CustomizationFailed](docs/vim.event.CustomizationFailed.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


Sysprep failed to run in the guest during customization. This will most like  have been caused by the fact that the wrong sysprep was used for the guest,  so we include the version information in the event.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| sysprepVersion | string | None | None | The version string for the sysprep files that were included in the  customization package. |
| systemVersion | string | None | None | The version string for the system |


