vim.profile.Profile.Description.Section
=======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.Profile.Description.Section.md">ProfileDescriptionSection</a> data object  contains a profile element description and any messages that may  be associated with the profile section.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| description | [vim.ExtendedElementDescription](vim.ExtendedElementDescription.md "vim.ExtendedElementDescription") | None | None | Localized message data. |
| message | [vmodl.LocalizableMessage](vmodl.LocalizableMessage.md "vmodl.LocalizableMessage") | true | None | List of messages that make up the section. |


