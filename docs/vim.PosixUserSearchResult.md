vim.PosixUserSearchResult
=========================
inherits from [vim.UserSearchResult](docs/vim.UserSearchResult.md)


Searching for users and groups on POSIX systems provides   User ID and Group ID information, in addition to that    defined in UserSearchResult.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | int | None | None | If the search result is for a user, then id refers to User ID. For a group,    the value of Group ID is assigned to id. |
| shellAccess | bool | true | None | If the search result is for a user, shellAccess indicates whether shell   access has been granted or not. |


