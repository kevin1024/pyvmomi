vim.host.SystemInfo
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Information about the system as a whole.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vendor | string | None | None | Hardware vendor identification. |
| model | string | None | None | System model identification. |
| uuid | string | None | None | Hardware BIOS identification. |
| otherIdentifyingInfo | [vim.host.SystemIdentificationInfo](vim.host.SystemIdentificationInfo.md "vim.host.SystemIdentificationInfo") | true | None | Other System identification information. This information may be vendor   specific |


