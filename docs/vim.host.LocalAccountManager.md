vim.host.LocalAccountManager
============================


This managed object type provides an interface   through which local accounts on a host are managed.  Note that this   managed object applies only to applications that use a local account   database on the host to provide authentication (ESX Server, for example).   POSIX and win32 hosts may impose different restrictions on the password,   ID, and description formats. POSIX host implementation may restrict the   user or group name to be lower case letters and less than 16 characters in   total.  It may also disallow characters such as   ";", "\n", and so on.  In short, all the platform dependent rules and   restrictions regarding naming of users/groups and password apply here.   An InvalidArgument fault is thrown if any of these rules are not obeyed.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


CreateUser([user](vim.host.LocalAccountManager.AccountSpecification.md "vim.host.LocalAccountManager.AccountSpecification"))
----------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists")

---
| service name | CreateUser |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Local.ManageUserGroups |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | if the specified local user account   already exists. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the user name or password has an   invalid format. |




UpdateUser([user](vim.host.LocalAccountManager.AccountSpecification.md "vim.host.LocalAccountManager.AccountSpecification"))
----------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.UserNotFound](vim.fault.UserNotFound.md "vim.fault.UserNotFound"), [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists")

---
| service name | UpdateUser |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Local.ManageUserGroups |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.UserNotFound](vim.fault.UserNotFound.md "vim.fault.UserNotFound") | if user is not found. |
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | if new account specification specifies an existing                         user's ID. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if new password or description has an invalid format. |




CreateGroup([group](vim.host.LocalAccountManager.AccountSpecification.md "vim.host.LocalAccountManager.AccountSpecification"))
------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists")

---
### Deprecated
As of vSphere API 5.1, local user groups are not supported   and group specific methods will throw NotSupported.

| service name | CreateGroup |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Local.ManageUserGroups |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | if specified local group already exists. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if group name is in invalid format. |




RemoveUser([userName](#string "string"))
----------------------------------------
 raises [vim.fault.UserNotFound](vim.fault.UserNotFound.md "vim.fault.UserNotFound"), [vmodl.fault.SecurityError](vmodl.fault.SecurityError.md "vmodl.fault.SecurityError")

---
| service name | RemoveUser |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Local.ManageUserGroups |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.UserNotFound](vim.fault.UserNotFound.md "vim.fault.UserNotFound") | if the specified userName does not exist. |
| [vmodl.fault.SecurityError](vmodl.fault.SecurityError.md "vmodl.fault.SecurityError") | if trying to remove the last local user with                         DCUI access,                         or if trying to remove the last local                         user with full administrative privileges,                         or if the system has encountered an error while                         trying to remove user's permissions.                         or if the account cannot be removed due to                         permission issues. |




RemoveGroup([groupName](#string "string"))
------------------------------------------
 raises [vim.fault.UserNotFound](vim.fault.UserNotFound.md "vim.fault.UserNotFound")

---
### Deprecated
As of vSphere API 5.1, local user groups are not supported   and group specific methods will throw NotSupported.

| service name | RemoveGroup |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Local.ManageUserGroups |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.UserNotFound](vim.fault.UserNotFound.md "vim.fault.UserNotFound") | if the specified groupName does not exist. |




AssignUserToGroup([user](#string "string"), [group](#string "string"))
----------------------------------------------------------------------
 raises [vim.fault.UserNotFound](vim.fault.UserNotFound.md "vim.fault.UserNotFound"), [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists")

---
### Deprecated
As of vSphere API 5.1, local user groups are not supported   and group specific methods will throw NotSupported.

| service name | AssignUserToGroup |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Local.ManageUserGroups |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.UserNotFound](vim.fault.UserNotFound.md "vim.fault.UserNotFound") | if the specified user or group does not exist. |
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | if the user is already a member of the target group. |




UnassignUserFromGroup([user](#string "string"), [group](#string "string"))
--------------------------------------------------------------------------
 raises [vim.fault.UserNotFound](vim.fault.UserNotFound.md "vim.fault.UserNotFound"), [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission")

---
### Deprecated
As of vSphere API 5.1, local user groups are not supported   and group specific methods will throw NotSupported.

| service name | UnassignUserFromGroup |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Local.ManageUserGroups |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.UserNotFound](vim.fault.UserNotFound.md "vim.fault.UserNotFound") | if the specified user or group does not exist. |
| [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission") | if the group is the only group to which the   user belongs. |




