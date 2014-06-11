vim.event.EventDescription
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object provides static, locale-specific strings for event objects.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| category | [vim.ElementDescription](vim.ElementDescription.md "vim.ElementDescription") | None | None | <a href="vim.event.EventDescription.EventCategory.md">Event Category enum</a> |
| eventInfo | [vim.event.EventDescription.EventDetail](vim.event.EventDescription.EventDetail.md "vim.event.EventDescription.EventDetail") | None | None | The event class description details. |
| enumeratedTypes | [vim.EnumDescription](vim.EnumDescription.md "vim.EnumDescription") | true | None | Localized descriptions of all enumerated types that are used for  member declarations in event classes. |


