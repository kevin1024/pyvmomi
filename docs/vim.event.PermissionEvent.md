vim.event.PermissionEvent
=========================
inherits from [vim.event.AuthorizationEvent](docs/vim.event.AuthorizationEvent.md)


This event records a permission operation.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entity | [vim.event.ManagedEntityEventArgument](vim.event.ManagedEntityEventArgument.md "vim.event.ManagedEntityEventArgument") | None | None | The entity to which the permission applied. |
| principal | string | None | None | The user name or group to which the permission was granted. |
| group | bool | None | None | Whether or not the principal was a group. |


