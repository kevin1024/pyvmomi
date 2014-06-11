vim.host.SystemIdentificationInfo
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This data object describes system identifying information of the host. This   information may be vendor specific.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| identifierValue | string | None | None | The system identification information |
| identifierType | [vim.ElementDescription](vim.ElementDescription.md "vim.ElementDescription") | None | None | The description of the identifying information.<br>See <a href="vim.host.SystemIdentificationInfo.Identifier.md">HostSystemIdentificationInfoIdentifier</a><br> |


