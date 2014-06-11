vim.AuthorizationManager
========================


This managed object provides operations to query and update   roles and permissions.   <p>   <b>Privileges</b> are the basic individual rights required to    perform operations.  They are statically defined and   never change for a single version of a product.  Examples   of privileges are &quot;Power on a virtual machine&quot;    or &quot;Configure a host.&quot;   <p>   <b>Roles</b> are aggregations of privileges, used for convenience.   For user-defined roles, the system-defined privileges, "System.Anonymous",   "System.View", and "System.Read" are always present.   <p>   <b>Permissions</b> are the actual access-control rules.  A   permission is defined on a ManagedEntity and   specifies the user or group (&quot;principal&quot;) to which    the rule applies. The role specifies the   privileges to apply, and the propagate flag    specifies whether or not the rule applies to sub-objects    of the managed entity.   <p>   A ManagedEntity may have multiple permissions,   but may have only one permission per user or group. If, when logging   in, a user has both a user permission and a group permission    (as a group member) for the same entity, then the   user-specific permission takes precedent.  If there is no   user-specific permission, but two or more group permissions   are present, and the user is a member of the groups, then the    privileges are the union of the specified roles.   <p>   Managed entities may be collected together into a &quot;complex entity&quot; for   the purpose of applying permissions consistently. Complex entities may have a   Datacenter, ComputeResource, or ClusterComputeResource as a parent, with other   child managed objects as additional parts of the complex entity:   <ul>     <li>A Datacenter's child objects are the root virtual machine and host Folders.     <li>A ComputeResource's child objects are the root ResourcePool and HostSystem.     <li>A ClusterComputeResource has only the root ResourcePool as a child object.   </ul>   Child objects in a complex entity are forced to inherit permissions from the   parent object. When query operations are used to discover permissions on child   objects of complex entities, different results may be returned for the owner of the   permission. In some cases, the child object of the complex entity is returned as   the object that defines the permission, and in other cases, the parent from which   the permission is propagated is returned as the object that defines the permission.   In both cases, the information about the owner of the permission is correct, since   the entities within a complex entity are considered equivalent.  Permissions   defined on complex entities are always applicable on the child entities,    regardless of the propagation flag, but may only be defined or modified on the   parent object.   <p>   In a group of fault-tolerance (FT) protected VirtualMachines, the secondary    VirtualMachines are forced to inherit permissions from the primary VirtualMachine.    Queries to discover permissions on FT secondary VMs always return the primary VM    as the object that defines the permissions. Permissions defined on an FT primary   VM are always applicable on its secondary VMs, but can only be defined or modified   on the primary VM.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='privilegeList'>privilegeList</a> | [vim.AuthorizationManager.Privilege](vim.AuthorizationManager.Privilege.md "vim.AuthorizationManager.Privilege") | true | System.View | The list of system-defined privileges. |
| <a href='roleList'>roleList</a> | [vim.AuthorizationManager.Role](vim.AuthorizationManager.Role.md "vim.AuthorizationManager.Role") | true | System.View | The currently defined roles in the system, including   static system-defined roles. |
| <a href='description'>description</a> | [vim.AuthorizationDescription](vim.AuthorizationDescription.md "vim.AuthorizationDescription") | None | System.View | Static, descriptive strings for system roles and privileges. |


AddAuthorizationRole([name](#string "string"), [privIds](#string "string"))
---------------------------------------------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists")

---
| service name | AddAuthorizationRole |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Authorization.ModifyRoles |
| return type | None |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | if a role with the given name already exists. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the role name is empty. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if privIds contains an unknown privilege. |




RemoveAuthorizationRole()
-------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.RemoveFailed](vim.fault.RemoveFailed.md "vim.fault.RemoveFailed"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | RemoveAuthorizationRole |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Authorization.ModifyRoles |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the role does not exist. |
| [vim.fault.RemoveFailed](vim.fault.RemoveFailed.md "vim.fault.RemoveFailed") | if failIfUsed is true and the role has permissions. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the role is a system role, meaning it cannot be                              changed. |




UpdateAuthorizationRole([newName](#string "string"), [privIds](#string "string"))
---------------------------------------------------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission"), [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UpdateAuthorizationRole |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Authorization.ModifyRoles |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the role does not exist, or if a privilege                             in the list cannot be found. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the new role name is empty. |
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | if another role with the given name already exists. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the role is a system role, meaning it cannot be                              changed. |
| [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission") | if current session does not have any privilege                             that being updated in the new role or                             "Authorization.ModifyRoles" privilege on the                             root folder. |




MergePermissions()
------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.AuthMinimumAdminPermission](vim.fault.AuthMinimumAdminPermission.md "vim.fault.AuthMinimumAdminPermission"), [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | MergePermissions |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Authorization.ReassignRolePermissions |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if either the source or destination role does not exist. |
| [vim.fault.AuthMinimumAdminPermission](vim.fault.AuthMinimumAdminPermission.md "vim.fault.AuthMinimumAdminPermission") | if srcRoleId is the Administrator role, meaning                             that applying the change would leave the system with                            no Administrator permission on the root node. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if dstRoleId is the View or Anonymous role or if                           both role IDs are the same. |
| [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission") | if current session does not have any privilege                            in the source or destination role or                            "Authorization.ReassignRolePermissions"                            privilege on the root folder. |




RetrieveRolePermissions()
-------------------------
 raises [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | RetrieveRolePermissions |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the role does not exist. |




RetrieveEntityPermissions([entity](vim.ManagedEntity.md "vim.ManagedEntity"))
-----------------------------------------------------------------------------
 raises [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound")

---
| service name | RetrieveEntityPermissions |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound") | if the entity does not exist. |




RetrieveAllPermissions()
------------------------

| service name | RetrieveAllPermissions |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




SetEntityPermissions([entity](vim.ManagedEntity.md "vim.ManagedEntity"), [permission](vim.AuthorizationManager.Permission.md "vim.AuthorizationManager.Permission"))
--------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.UserNotFound](vim.fault.UserNotFound.md "vim.fault.UserNotFound"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound"), [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound"), [vim.fault.AuthMinimumAdminPermission](vim.fault.AuthMinimumAdminPermission.md "vim.fault.AuthMinimumAdminPermission"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission")

---
| service name | SetEntityPermissions |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.UserNotFound](vim.fault.UserNotFound.md "vim.fault.UserNotFound") | if a given user or group does not exist. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if a permission's roleId is not valid. |
| [vim.fault.AuthMinimumAdminPermission](vim.fault.AuthMinimumAdminPermission.md "vim.fault.AuthMinimumAdminPermission") | if this change would leave the system with                            no Administrator permission on the root node, or it                            would grant further permission to a user or group who                            already has Administrator permission on the root node. |
| [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound") | if the given entity does not exist. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if one of the new role IDs is the View or                            Anonymous role, or the entity does not support assigning                            permissions. |
| [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission") | if current session does not have any privilege                            in any permission that being set or                            "Authorization.ModifyPermissions" privilege on                            the entity. |




ResetEntityPermissions([entity](vim.ManagedEntity.md "vim.ManagedEntity"), [permission](vim.AuthorizationManager.Permission.md "vim.AuthorizationManager.Permission"))
----------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.UserNotFound](vim.fault.UserNotFound.md "vim.fault.UserNotFound"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound"), [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound"), [vim.fault.AuthMinimumAdminPermission](vim.fault.AuthMinimumAdminPermission.md "vim.fault.AuthMinimumAdminPermission"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission")

---
| service name | ResetEntityPermissions |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.UserNotFound](vim.fault.UserNotFound.md "vim.fault.UserNotFound") | if one of the given users or groups does not exist. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if a permission for this entity and user or group                        does not exist. |
| [vim.fault.AuthMinimumAdminPermission](vim.fault.AuthMinimumAdminPermission.md "vim.fault.AuthMinimumAdminPermission") | if this change would leave the system with                            no Administrator permission on the root node, or it                            would grant further permission to a user or group who                            already has Administrator permission on the root node. |
| [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound") | if the given entity does not exist. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if one of the new role IDs is the View or                            Anonymous role, or the entity does not support                             assigning permissions. |
| [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission") | if current session does not have any privilege                            in the updated permission or                            "Authorization.ModifyPermissions" privilege on                            the entity. |




RemoveEntityPermission([entity](vim.ManagedEntity.md "vim.ManagedEntity"), [user](#string "string"))
----------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.AuthMinimumAdminPermission](vim.fault.AuthMinimumAdminPermission.md "vim.fault.AuthMinimumAdminPermission"), [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | RemoveEntityPermission |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if a permission for this entity and user or group                        does not exist. |
| [vim.fault.AuthMinimumAdminPermission](vim.fault.AuthMinimumAdminPermission.md "vim.fault.AuthMinimumAdminPermission") | if this change would leave the system with                            no Administrator permission on the root node. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if one of the new role IDs is the View or                            Anonymous role, or the entity does not support                             removing permissions. |
| [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission") | if current session does not have any privilege                            in the permission to be removed or                            "Authorization.ModifyPermissions" privilege                            on the entity. |




HasPrivilegeOnEntity([entity](vim.ManagedEntity.md "vim.ManagedEntity"), [sessionId](#string "string"), [privId](#string "string"))
-----------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound")

---
| service name | HasPrivilegeOnEntity |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#None) |
| privilege    | System.View |
| return type | [bool](bool.md "bool") |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound") | if the given entity does not exist. |




HasPrivilegeOnEntities([entity](vim.ManagedEntity.md "vim.ManagedEntity"), [sessionId](#string "string"), [privId](#string "string"))
-------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound")

---
| service name | HasPrivilegeOnEntities |
|:--|:--|
| since version | [vSphere API 5.5](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound") | if a given entity does not exist. |




