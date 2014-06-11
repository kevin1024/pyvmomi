vim.event.PermissionAddedEvent
==============================
inherits from [vim.event.PermissionEvent](docs/vim.event.PermissionEvent.md)


This event records the creation of a permission.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| role | [vim.event.RoleEventArgument](vim.event.RoleEventArgument.md "vim.event.RoleEventArgument") | None | None | The associated role. |
| propagate | bool | None | None | Whether or not the permission applies to sub-entities. |


