vim.event.CustomFieldValueChangedEvent
======================================
inherits from [vim.event.CustomFieldEvent](docs/vim.event.CustomFieldEvent.md)


This event records a change to a custom field value for a particular entity.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entity | [vim.event.ManagedEntityEventArgument](vim.event.ManagedEntityEventArgument.md "vim.event.ManagedEntityEventArgument") | None | None | The entity on which the field value was changed. |
| fieldKey | int | None | None | The custom field whose value was changed for the entity. |
| name | string | None | None | The name of the custom field at the time the value was changed. |
| value | string | None | None | The new value that was set. |


