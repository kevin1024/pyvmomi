vim.UserSearchResult
====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


When searching for users, the search results in   some additional information. This object describes   the additional information.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| principal | string | None | None | Login name of a user or the name of a group. This key is   the user within the searched domain. |
| fullName | string | true | None | Full name of the user found by the search, or the description   of a group, if available. |
| group | bool | None | None | If this is true, then the result is a group. If this is false, then the    result is a user. |


