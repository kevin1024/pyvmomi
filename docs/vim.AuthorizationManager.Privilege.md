vim.AuthorizationManager.Privilege
==================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type provides access to some aspect of the system.   Privileges are generally independent. This means a user with a privilege    usually can perform an associated set of actions without needing any    additional supporting privileges.   <p>   Within each product version, privileges do not change.    See <a href="vim.AuthorizationDescription.md">AuthorizationDescription</a> for   detailed information on the privileges defined by the system.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| privId | string | None | None | Unique identifier. |
| onParent | bool | None | None | Determines whether or not the privilege is applied on the parent entity. |
| name | string | None | None | Privilege name. |
| privGroupName | string | None | None | Group name. |


